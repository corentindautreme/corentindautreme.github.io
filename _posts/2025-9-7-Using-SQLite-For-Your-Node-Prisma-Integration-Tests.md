---
layout: post
title: Using SQLite for your Node.js/Prisma integration tests
---

I recently tried my hand at Node.js backend development after over 6 years of Sping Boot work experience. I was looking
to reproduce a familiar behavior: the injection of a local, temporary database into my integration tests for my Prisma
ORM layer to interact with. I couldn't find an out-of-the-box solution for this, but eventually found a way, using Jest
mocks and SQLite - here's how.

<!--more-->

## A database for my ITs

My goal was to have, on the environment on which my integration tests would run, a temporary local database that would
be seeded with test data and injected into my code to "override" my actual database (in my case, Postgres) for my Prisma
ORM layer to interact with, just for the duration of the tests - not unlike what you can achieve in a Spring Boot
application with JPA and H2.

// diagram (
mermaid?) https://stackoverflow.com/questions/53883747/how-to-make-github-pages-markdown-support-mermaid-diagram

```mermaid
flowchart LR
    Start --> Stop
```

The issue with Prisma is that you have to specify the target platform in the configuration of your client, which means
that a client generated from a Prisma schema targeting Postgres cannot be reused to interact with another database
engine.

Since I wasn't exactly planning on propping up and tearing down a full PostgreSQL cluster everytime I want to run my
ITs, I had to find a way to work around that.

As to DB engine choice, Prisma ORM supports SQLite, which seems local and light enough for my use case.

So, the target was to have Prisma target my PostgreSQL database during normal runs of my application, and a local SQLite
database during my ITs.

## Adjusting the Prisma schema

Let's start by manually getting a Prisma that works for SQLite. In its current state, my schema isn't ready to target
SQLite: the `provider` is a massive giveaway, but as we'll see later, it isn't the only blocker:

```
datasource db {
  provider = "postgresql"
  ...
}
```

Let us copy my `schema.prisma` to `schema.integration.test.prisma`:

```bash
cp prisma/schema.prisma prisma/schema.integration.test.prisma
```

Now, let's make our first few adjustments:

* We change the `provider` from `postgresql` to `sqlite`
* We manually fix the URL of our database (for now) to a local `.db` file
* We also change the `output` of the generated client so that it doesn't override our "live" PostgreSQL client - this
  will allow us to test our SQLite client without overriding our "live" PostgreSQL one, and, later, to alternate between
  running our integration tests and serving a local app without having to regenerate a client everytime

```
generator client {
  provider = "prisma-client-js"
  - output   = "../generated/prisma"
  + output   = "../generated/integration/prisma"
}

datasource db {
  - provider = "postgresql"
  + provider = "sqlite"
  - url      = env("DATABASE_URL")
  + url      = "file:it.db"         // don't forget the "file:" prefix
}
```

At a glance, that should be it. We can try, **as long as we don't forget to specify a schema in your command**, to
push this schema to an SQLite database located in the `ìt.db` file using the prisma CLI to test it. Again, **let's not
forget to tell Prisma to use our "integration" schema, using the `--schema` argument**:

```bash
prisma db push --schema prisma/schema.integration.test.prisma
```

Now, depending on how large our schema is, we'll likely see quite a few errors. In my case, they were the following
ones:

* `error: Error validating model "<table>": You defined a database name for the primary key on the model. This is not supported by the provider.`
* `error: Native type VarChar is not supported for sqlite connector.`
* `error: Error parsing attribute "@relation": Your provider does not support named foreign keys.`

Some of these can be tricky, but after some digging, here's what I found:

* SQLite doesn't support giving your constraints (primary key, foreign key, etc.) a name; such namings are defined with
  `map: "<constraint_name>"` in the Prisma schema syntax
* Prisma doesn't support the usage of `@db` native types with SQLite, even if you try to use one of the very few
  types that SQLite supports:

```
error: Native type TEXT is not supported for sqlite connector.
```

_This is the error you obtain when trying to use native type `@db.TEXT`, even though `TEXT` is a valid SQLite type_

To move forward, we have to let
Prisma [automatically map our columns to the right SQLite type](https://www.prisma.io/docs/orm/overview/databases/sqlite#type-mapping-between-sqlite-to-prisma-schema),
and drop all of our custom constraint names; for example:

```
model departure
{
  - id        Int       @id(map: "departure_pk") @default(autoincrement())
  + id        Int       @id() @default(autoincrement())

  - direction String?   @db.VarChar
  + direction String?

  - time_utc  DateTime? @db.Time(6)
  + time_utc  DateTime?

  - line      line?     @relation(fields: [id_line], references: [id], onDelete: NoAction, onUpdate: NoAction, map: "fk_line")
  + line      line?     @relation(fields: [id_line], references: [id], onDelete: NoAction, onUpdate: NoAction)

  ...
}
```

Let's try to push our schema one more time, and hurray! No more error!

```bash
$ prisma db push --schema prisma/schema.integration.test.prisma 
Environment variables loaded from .env
Prisma schema loaded from prisma/schema.integration.test.prisma
Datasource "db": SQLite database "it.db" at "file:it.db"

SQLite database it.db created at file:it.db

🚀  Your database is now in sync with your Prisma schema. Done in 168ms

✔ Generated Prisma Client (v6.14.0) to ./generated/integration/prisma in 78ms
```

We have now successfully generated a SQLite database and had our Prisma schema re-created there, and Prisma generated a
client for us.

## Injecting the SQLite database into your tests

What we now want is for our integration tests to interact with our local SQLite database rather than our live PostgreSQL
one.

If you followed
the [Prisma docs](https://www.prisma.io/docs/orm/prisma-client/setup-and-configuration/databases-connections#prismaclient-in-long-running-applications),
you have only one Prisma client defined and exported for your whole application, that you re-import wherever you need
it. I did: my Prisma client is instantiated and exported in `lib/db/client.ts`:

```typescript
import { PrismaClient } from '../../../generated/prisma';

const prisma = new PrismaClient();

export default prisma;
```

This setup allows us to use **Jest** to mock the `lib/db/client` module by:

* creating a `__mocks__/` directory under `lib/db/`, that contains a `client.ts` file in which we export the object
  that will be used to mock our Prisma client
* enabling this mock before we run our tests by instructing Jest to, with a call to `jest.mock()`

What we'll do here is that we'll "replace" our live Prisma client by

1. creating an instance of the Prisma client that we generated from our "integration" schema
2. exposing it as the mock of our Prisma client in `__mocks__/client.ts`.
3. instructing Jest to inject this "mock" at the beginning of our test suite

Here's my `lib/db/__mocks/client.ts`:

```typescript
import { PrismaClient } from '../../../generated/integraton/prisma';    // note the change in the import - we want the "integration" client here!

const prisma = new PrismaClient();

export default prisma;
```

Now, let's write a quick test to try this out.

My app has a `LinesService` class that interacts with my unique Prisma client to retrieve data about public transport
lines. I know for a fact that my development Postgres database contains data in the `line` table, so this test, which
doesn't yet make use of our Prisma client "mock" (aka, the one that targets our SQLite database), should fail:

```typescript
import LinesService from '../src/services/lines.service';

const linesService = new LinesService();

describe('My integration tests', () => {
    it('should query my SQLite "mock" and thus return 0 rows', async () => {
        const lines = await linesService.prismaClient.line.findMany();
        expect(lines).toHaveLength(0);
    });
})
```

Running it results indeed in a failure:

```
Error: expect(received).toHaveLength(expected)

Expected length: 0
Received length: 14
Received array:  [{"id": 1, "name": "3", "type": "tram"}, {"id": 6, "name": "107", "type": "trolleybus"}, …]
```

Now, if I add a `jest.mock()` instruction to kindly ask Jest to use my SQLite Prisma client rather than my real Prisma
client:

```typescript
import LinesService from '../src/services/lines.service';

jest.mock('../src/lib/db/client');  // **new**

const linesService = new LinesService();

describe('My integration tests', () => {
    it('should query my SQLite "mock" and thus return 0 rows', async () => {
        const lines = await linesService.prismaClient.line.findMany();
        expect(lines).toHaveLength(0);
    });
});
```

, my SQLite database is instead queried, making the test pass, since my table is empty.

![_config.yml]({{ site.baseurl
}}/images/articles/2025-9-7-Using-SQLite-For-Your-Node-Prisma-Integration-Tests/passed_test.png)

We can of course seed our tables first, to create meaningful test cases:

```typescript
describe('My integration tests', () => {
    beforeAll(async () => {
        await linesService.prismaClient.line.create({data: {id: 1, name: 'Line'}});
    });

    it('should query my SQLite "mock" and thus return 0 rows', async () => {
        const lines = await linesService.prismaClient.line.findMany();
        expect(lines).toHaveLength(1);
        expect(lines[0].name).toEqual('Line');
    });

    afterAll(async () => {
        await linesService.prismaClient.line.deleteMany();
    });
});
```

## Automating it all

We earlier created a Prisma schema for our integration tests manually. But manually maintaining 2 separate Prisma
schemas isn't only tedious, it's also error-prone (changing something in one but not in the other, etc.). I would argue
these 2 arguments are enough to qualify this as a terrible idea.

Ideally, we'd want 1) our "integration" schema to be generated from the current version of our Prisma schema 2) our SQLite
database created and 3) an "integration" Prisma client generated, all right before running our tests.

The detailed steps for this would be:

* Creating a copy of the Prisma schema file
* In the copied schema file:
    * Update the output generation directory
    * Change the provider to `sqlite`
    * Remove the naming instruction from all constraints
    * Remove all `@db.*` native type instructions
* Set the SQLite database up using the "integration" schema file we've just prepared
* Generate a Prisma client and export it as a "mock" of the real Prisma client

Let's start by deleting the `prisma/schema.integration.prisma` file and the `generated/integration/prisma/` directory:
we'll be (re)generating them automatically from now on.

Next, let's go back to our Prisma client "mock" definition to include the "integration" schema file creation, client
generation, and database setup logic:

```typescript
import { execSync } from 'child_process';
import { join } from 'path';
import * as fs from 'node:fs';

const schema = join(__dirname, '..', '..', '..', '..', 'prisma', 'schema.prisma');
const integrationSchema = join(__dirname, '..', '..', '..', '..', 'prisma', 'schema.integration.test.prisma');

const schemaContent = fs.readFileSync(schema, 'utf8');

// update our "integration" schema to set the right provider, adjust the schema definition to SQLite, etc.
const schemaForIntegration = schemaContent
    .replace(/generated\/prisma/g, 'generated/integration/prisma')  // instruct the Prisma client to be generated in a separate directory
    .replace(/postgresql/g, 'sqlite')                               // change the provider from 'postgresql' to 'sqlite'
    .replace(/(, )*map: "[A-Za-z0-9_]+"/g, '')                      // remove naming instructions from keys and constraints
    .replace(/@db\.[A-Za-z0-9()]+/g, '')                            // remove @db native type instructions
    .replace(/onDelete: NoAction/g, 'onDelete: Cascade');           // cascade delete on FKs to ease post-suite clean up
fs.writeFileSync(integrationSchema, schemaForIntegration, 'utf8');

// generate the SQLite .db file next to the Prisma schema files
const dbPath = join(__dirname, '..', '..', '..', '..', 'prisma', 'dev.db');

// set DATABASE_URL to the SQLite database URL (file:path/to/sqlite/file.db)
const url = `file:${dbPath}`;
process.env.DATABASE_URL = url;

const prismaBinary = join(__dirname, '..', '..', '..', '..', 'node_modules', '.bin', 'prisma');

// generate a Prisma client for our SQLite database using the Prisma CLI and our "integration" schema
execSync(`${prismaBinary} generate --schema ${integrationSchema}`);

import { PrismaClient } from '../../../../generated/integration/prisma';

const prisma = new PrismaClient();

// export the SQLite Prisma client as our "mock" Prisma client
export default prisma;

// set up/tear down the SQLite database
beforeAll(() => {
    execSync(`${prismaBinary} db push --schema ${integrationSchema}`, {
        env: {
            ...process.env,
            DATABASE_URL: url,
        }
    });
});

afterAll(async () => {
    await prisma.$disconnect();
    execSync(`rm ${dbPath}`);
});
```

Besides generating our "mock" Prisma client, we now automatically do everything that we did manually earlier, namely:

* Copying our schema file and adjusting it to work with SQLite
* Setting up the SQLite database using the Prisma CLI

That should be it, right? Well, if we try re-running our previous test, we hit an error:

```
  ● Test suite failed to run

    src/lib/db/__mocks__/client.ts:31:38 - error TS2307: Cannot find module '../../../../generated/integration/prisma' or its corresponding type declarations.

    31 import { Prisma, PrismaClient } from '../../../../generated/integration/prisma';
                                            ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
```

Uh-oh. In our "mock" definition, we try to import our generated client. But at Typescript compilation time, we haven't
yet generated it!

Luckily, there's a (dirty) workaround for that: we can create a "dummy" module in an `index.ts` file under
`/generated/integration/prisma` with just enough definitions to allow our code to compile. Since Prisma generates raw
Javascript, it will never override `index.ts`.

If we create `/generated/integration/prisma/index.ts` and fill it with the following content, the code compiles again -
and our test passes once more:

```typescript
export class PrismaClient {
    constructor() {
    };

    $disconnect = () => {
        return new Promise(() => {
        })
    };
}
```

## Final words

If, like me, you were struggling to replace a real database with a local one in your Node.js/Prisma integration tests, I
hope this post has been of use to you.

You can see a real-life implementation of this
technique [in this repo of mine](https://github.com/corentindautreme/transit-planner/pull/20/files). You'll find that
certain things are every so slightly different here and there (with dirty and useless extra bits here I there I
realize), but nothing too too far off.

Please note that SQLite may not order the results in the same way as other database platforms would. You might want to
adjust your assertions so that this doesn't break your tests.

As a final tip, if you're looking to empty (aka truncate) all tables of an SQLite database (to clear out seeded data in
between tests suites, for example), you can use the following code. You'll need to update your "dummy" Prisma
definitions to make sure that `$queryRaw` and `$executeRow` are functions of `PrismaClient`, and `raw` a function of
`Prisma`:

```typescript
const tables = await prisma.$queryRaw`SELECT name
                                          FROM sqlite_master
                                          WHERE type = 'table'
                                            AND name NOT LIKE 'sqlite_%'` as { name: string }[];
for (const table of tables) {
    await prisma.$executeRaw`DELETE
                                 FROM ${Prisma.raw(table.name)}`;
}
```