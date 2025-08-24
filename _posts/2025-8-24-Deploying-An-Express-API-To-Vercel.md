---
layout: post
title: Deploying an Express API to Vercel
---

One summer, I developed a small Node.js API using Express. It turned out useful and I wanted to host it for my personal usage. I turned to Vercel, and struggled for a while to get my Express API running on there. In this post, I go over how I eventually managed, as well as a few considerations that are worth keeping in mind when choosing Vercel for this use case. 

<!--more-->

If you're just here for the solution, jump directly to [TLDR - how to host an Express API to Vercel](#tldr---how-to-host-an-express-api-to-vercel).

If you are curious, or want to know more about the whole Express hosting on Vercel thing, feel free to read on. Personally, I've spent a few hours copy-pasting stuff that didn't work like a monkey, so at that point, I'd probably want to read this. In any case - good luck!

### Should you even do that?

Maybe yes. Probably not.

The only way to deploy an Express API to Vercel is by hosting it through Vercel's [Functions](https://vercel.com/docs/functions) feature, designed for so-called <span class="tooltip-toggle" aria-label="I hate this name with a passion lol. Oh yeah, serverless? Then where the f%ck is the code running, Benjamin*?">serverless functions</span><span class="tooltip-toggle" aria-label="(*)I like to use the name of someone I'm particularily annoyed with in these. Recently, I've felt particularily annoyed with a dude named Benjamin."> -</span> which is not what you built.

Among other things, if your hosted API hasn't been called for a while, the Vercel Function will "cold start" upon receiving a new request, AKA it will boot up a brand new Express app and redirect the request to it; not only does this take a few seconds, it also means you can kiss any kind of server-side caching goodbye.

There can be reasons why you'd want to host a backend Node.js API on Vercel, though. Mine was to host, at no cost, a small but rather useful side project that I wanted to access away from my laptop. Vercel offering an AWS-like free tier through their [Hobby Plan](https://vercel.com/docs/plans/hobby), and me having both a prior experience with Vercel and a strong desire not to spend a dime on my side projects, Vercel sounded like a no-brainer.

But if you're looking to host a production grade API aiming to serve more than a dozen users, then I'm afraid hosting an Express API on Vercel is far from being the best solution. But hey, I'm not your mom, you do you.

### Vercel Hobby Plan considerations

Once you've hit the limits offered by the Vercel's [Hobby Plan](https://vercel.com/docs/plans/hobby), you're done: you won't be able to access the features if your app that relies on the limit(s) you've reached.

So, if someone bazooka-izes your Express endpoints with enough requests to max out, say, your Function Invocations allowance, your API will remain inaccessible to anyone, including yourself, until your plan's limits reset.

If you intend to keep access to your hosted application at any time, you might want to restrict and/or deny access to certain parts of your application.

* Once deployed: you should look into Vercel's [Firewall](https://vercel.com/docs/vercel-firewall) and set up rules to restrict and/or deny access to your application. For example, you could straight up deny requests that do not emanate from a restricted list of IPs. Or, you could set up [rate limiting](https://vercel.com/docs/vercel-firewall/vercel-waf/rate-limiting) to allow access to a resource, but not too often.
* Before deploying: add a layer of authentication and/or authorization. While this won't directly help with keeping your resource usage in check, it's a pretty damn good practice <span class="tooltip-toggle" aria-label="One of my law professors always used to say: 'Posting something to social media is just like publishing it on the front page of the Le Monde'. I've personally decided to apply that to anything I host on the internet.">whenever hosting something online</span>, and it could save you a few undesired extra function calls.

### TLDR - how to host an Express API to Vercel

Here's the short answer. If this doesn't work, or you have more questions, or you want more details, keep reading this post, as I go more into depth later on.
 
**⚠️ When I say "_at the root of your project_" below, I mean it - these should be at the same level as your package.json file, and NOT inside of your src/ directory (if you have one)**

* **At the root of your project**, have a `/api` directory, containing an **index.js** (or .ts) file that exports your Express `app` instance
* **At the root of your project**, have a `/public` directory. Include an empty `.gitkeep` file so that Git lets you commit it
* **At the root of your project**, have a `vercel.json` file with the following content:

```json
{
  "$schema": "https://openapi.vercel.sh/vercel.json",
  "rewrites": [
    {
      "source": "/(.*)",
      "destination": "/api"
    }
  ]
}
```

* **On Vercel**: use the following configuration for your project:
  * **Framework Settings**
    * Framework Preset: **"Other"**
      * Build Command: **(leave empty)**
      * Output Directory: **(leave empty)**
      * Install Command: **(leave empty)**
      * Development Command: **(leave empty)**
  * **Root Directory**
    * **(leave empty)**

So, to recap:
* This is what your project source might look like:

```json
.
└── .git
└── api
│   └── index.js|ts     <-- mandatory
└── dist                
└── generated
└── node_modules
└── prisma
└── public
│   └── .gitkeep        <-- mandatory
└── src
│   └── app.ts
│   └── server.ts
└── test
└── package.json
└── pnpm-lock.yaml
└── README.md
└── tsconfig.json
└── vercel.json         <-- mandatory
```

ℹ️ _What's not flagged as "mandatory" was only left as an example, to give some extra context_

* This is what your Vercel project config **MUST** look like:

![_config.yml]({{ site.baseurl }}/images/articles/2025-8-24-Deploying-An-Express-API-To-Vercel/vercel_project_build_config.png)

__________

You're still here? Hi! In the below sections, we'll go over what is written in the previous TDLR section, but in more details.

### The `api/index.js|ts` file

Vercel expects to find a Node.js function under a `/api` directory, which is why an `index.ts` (or `.js`) file is needed in a directory named `/api`, that needs to be located \***at the root of your project**\*.

**⚠️ When I say "_at the root of your project_", I mean it - these should be at the same level as your package.json file, and NOT inside of your src/ directory (if you have one)**

This file only needs to expose the Express **app** object of your project, that is, the object returned when calling `express()`:

```typescript
const app = express();
```

**⚠️ Note that you don't want to expose your HTTP server object, but the **app**. Vercel does not need your server logic - it has its own to handle Function invocations**

Here's what my `index.ts` file looks like:

```typescript
import app from '../src/app';

export default app;
```

I chose to put my Express source code in a `src/` directory, at the root my of project (you might see a lot of people do that). My `app` object is defined, **and exported**, in `src/app.ts`. I simply import the app object from `src/app.ts` in my `api/index.ts`, and immediately re-export it to make it available to Vercel.

```json
.
└── api             **new**
│   └── index.ts    **new**
└── ...
└── src
│   └── ...
│   └── app.ts
│   └── server.ts
```

If your `app` object is defined in an `app.js` file at the root of your project, like the ["Hello World" example from the Express docs](https://expressjs.com/en/starter/hello-world.html), simply add an export instruction for your `app` object and adjust the import in your `api/index.js|ts` file:

**app.js**
```javascript
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => {
  res.send('Hello World!');
})

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`);
})

export default app;     // Don't forget to export your app object!
```

**api/index.js**
```javascript
import app from '../app';

export default app;
```

Your project would look like this in this case:
```json
.
└── api             **new**
│   └── index.js    **new**
└── app.js
└── ...
```

### The `public/` directory

When developing a backend application with Express, you only need a `public/` directory if you wish to expose static assets (such as images, favicons, etc.).

However, Vercel would really, really like to find a `public/` directory \***at the root of your project**\* (and **NOT** in `src/`!). If you don't include one, your Vercel build will fail and print out this error log:

```text
Error: No Output Directory named "public" found after the Build completed. You can configure the Output Directory in your Project Settings.
Learn More: https://vercel.link/missing-public-directory
```

I would advise against playing with your Output Directory settings as Vercel suggests. Instead, create a `public/` directory \***at the root of your project**\* (and **NOT** in `src/`!). If you're like me and are using Git(hub), you'll find that Git will not push an empty `public/` directory. You can force Git to push your directory by adding a special empty file named `.gitkeep` to your `public/` directory:

```json
.
└── api
│   └── index.ts
└── public          **new**
│   └── .gitkeep    **new**
└── ...
└── src
│   └── ...
```

### The `vercel.json` file

The `vercel.json` is required to properly redirect incoming calls to your Express app. If you don't create it, you'll end up with this error - and the docs will be of no help (trust me, I've been there).

![_config.yml]({{ site.baseurl }}/images/articles/2025-8-24-Deploying-An-Express-API-To-Vercel/vercel_404_not_found.png)

\***At the root of your project**\* (and **NOT** in `src/`!), create a `vercel.json` file with the following content:

```json
{
  "$schema": "https://openapi.vercel.sh/vercel.json",
  "rewrites": [
    {
      "source": "/(.*)",
      "destination": "/api"
    }
  ]
}
```

This [instructs Vercel to redirect all incoming calls](https://vercel.com/docs/rewrites) to /api (and thus our Express app).

At this step, your project should include all of this:

```json
.
└── api
│   └── index.ts
└── public
│   └── .gitkeep
└── vercel.json   **new**
└── ...
```

You now have everything you need to deploy your Express API to Vercel - so let's get to it, shall we?

### Deploying to Vercel

> :information_source: The below assumes you're using GitHub to host your code repository and that you've pushed all the changes described above to your repository.

From your Vercel dashboard, click on the "Add New..." button in the top right corner and select "Project".

![_config.yml]({{ site.baseurl }}/images/articles/2025-8-24-Deploying-An-Express-API-To-Vercel/vercel_add_new_project.png)

Under "Import Git Repository", find the repository of your project and click "Import".

![_config.yml]({{ site.baseurl }}/images/articles/2025-8-24-Deploying-An-Express-API-To-Vercel/vercel_import_git_repository.png)

On the next page ("New Project"), make sure the follow settings are set (they should be by default):

* **Framework Preset**: `Other`
* **Root Directory**: `./`
* Under **Build and Output Settings** (unfold just under the "Root Directory" field):
  *  **Build Command**: _(empty)_ (you should see the following greyed-out placeholder: `'npm run vercel-build' or 'npm run build'`)
  *  Output Command: _(empty)_ (you should see the following greyed-out placeholder: `'public' if it exists, or '.'`)
  *  Install Command: _(empty)_ (you should see the following greyed-out placeholder: `'yarn install', 'pnpm install', 'npm install', or 'bun install'`)

![_config.yml]({{ site.baseurl }}/images/articles/2025-8-24-Deploying-An-Express-API-To-Vercel/vercel_new_project.png)

Click on "Deploy", let Vercel build and deploy your API, and after a little while, it should eventually congratulate you, and invite you to "Continue to Dashboard".

![_config.yml]({{ site.baseurl }}/images/articles/2025-8-24-Deploying-An-Express-API-To-Vercel/vercel_congratulations.png)

Do continue to the dashboard using the button, and click either the "Visit" button in the top right, or the link under "Domains", to access your API.

![_config.yml]({{ site.baseurl }}/images/articles/2025-8-24-Deploying-An-Express-API-To-Vercel/vercel_dashboard.png)

Now if you're like me, you might not have anything exposed at `/`, resulting in the following response in your browser:

```text
Cannot GET /
```

However, navigating to one of your endpoints should return something more familiar:

![_config.yml]({{ site.baseurl }}/images/articles/2025-8-24-Deploying-An-Express-API-To-Vercel/vercel_example_endpoint.png)

That should be it - your Express API should now be deployed to Vercel!

### Troubleshooting

#### Check out a working project

I've had all sorts of issues, from DEPLOYMENT NOT FOUND to NOT FOUND to build failures. I've eventually landed on the right config on [this project](https://github.com/corentindautreme/transit-planner). I also made sure to implement my Vercel configuration [in a separate PR](https://github.com/corentindautreme/transit-planner/pull/10), which might be of use to you if you're, like me, trying to deploy an existing project to Vercel.

#### Make sure you have the necessary files and directories, at the right location, with the right content

The `api/` directory, `public/` directory, and `vercel.json` file are ALL mandatory, and they ALL need to be placed **at the root of your project**. That means **NOT** in your `src/` directory if you have one.

The below project setup is wrong and will not result in a successful deployment of your Express app on Vercel:

```json
.
└── .git
└── dist                
└── generated
└── node_modules
└── src
│   └── api               ❌ WRONG: your api/ directory needs to be placed at the **root of your project**, not in src/
│   │   └── index.js|ts   ❌
│   └── public            ❌ WRONG: your public/ directory needs to be placed at the **root of your project**, not in src/
│   │   └── .gitkeep      ❌
│   └── app.ts
│   └── server.ts
│   └── vercel.json       ❌ WRONG: your vercel.json file needs to be placed at the **root of your project**, not in src/
└── test
└── package.json
└── pnpm-lock.yaml
└── README.md
└── tsconfig.json
```

#### Review your deployment settings

Review, and if needed, adjust your project's Build and Deployment settings on Vercel.

You can access these for an existing Vercel project as follows:

From your [Vercel dashboard](https://vercel.com/):
* Under "Projects", click on your project

![_config.yml]({{ site.baseurl }}/images/articles/2025-8-24-Deploying-An-Express-API-To-Vercel/vercel_dashboard_projects.png)

* At the top of the page, navigate to the "Settings" tab

![_config.yml]({{ site.baseurl }}/images/articles/2025-8-24-Deploying-An-Express-API-To-Vercel/vercel_project.png)

* From the left menu, select "Build and Deployment", and make sure your configuration matches the following:

  * **Framework Settings**
    * **Framework Preset**: `Other`
    *  **Build Command**: _(empty)_ (you should see the following greyed-out placeholder: `'npm run vercel-build' or 'npm run build'`)
    *  Output Command: _(empty)_ (you should see the following greyed-out placeholder: `'public' if it exists, or '.'`)
    *  Install Command: _(empty)_ (you should see the following greyed-out placeholder: `'yarn install', 'pnpm install', 'npm install', or 'bun install'`)
    *  Development Command: _(empty)_ (you should see the following greyed-out placeholder: `None`)
  * **Root Directory**: _(empty)_

![_config.yml]({{ site.baseurl }}/images/articles/2025-8-24-Deploying-An-Express-API-To-Vercel/vercel_project_settings.png)
