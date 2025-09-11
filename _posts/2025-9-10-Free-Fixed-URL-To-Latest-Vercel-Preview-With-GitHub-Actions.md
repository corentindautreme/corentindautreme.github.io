---
layout: post
title: Free Fixed URL to your latest Vercel preview with GitHub Actions
---

On small scale projects hosted on Vercel, it can be useful to have a fixed URL that always points to the latest preview
deployment. One can easily achieve this - at no cost! - using GitHub Actions' `repository_dispatch` events emitted by
Vercel, as well as the Vercel CLI, to create a free Vercel custom domain upon successful deployment to your Preview
environment.

<!--more-->

![_config.yml]({{ site.baseurl
}}/images/articles/2025-9-11-Free-Fixed-URL-To-Latest-Vercel-Preview-With-GitHub-Actions/vercel_preview_url.png)

_The `transit-planner-client-preview.vercel.app` domain was automatically created when this build was deployed to my
Preview environment_

Despite constantly checking how my webapps look on mobile using my browser's dev tools, I regularly got a few surprises
once checking the final deployed result on an actual device.

While Vercel kindly exposes various URLs to access a preview deployment, these URLs, despite following a predictable
pattern, change with every deployment - making them unusable in some situations, such as applications with a
callback-based third-party authentication layer.

![_config.yml]({{ site.baseurl
}}/images/articles/2025-9-11-Free-Fixed-URL-To-Latest-Vercel-Preview-With-GitHub-Actions/uri_mismatch.png)

_Ah yes silly me, I completely forgot to whitelist
my-web-application-git-fe-dfe98e7-corentindautremes-projects.vercel.app as a valid redirection URI, how could I be so
forgetful_

Now if you could always access your latest Vercel preview deployment with a fixed, never-changing URL, like
_my-web-application-preview.vercel.app_, you could add this URL to the redirection whitelist of your OAuth provider.
Lucky you, that's exactly what we're going to set up today.

## Vercel custom domains (aka aliases)

Vercel allows you to create custom domains that target a specific deployment, by attaching the domain to an environment,
and a branch (if the selected environment is Preview). That means that you could, after each new deployment of a branch
to your Preview environment, log in to Vercel and manually create and attach a custom domain to your Preview environment
and deployed branch.
Yawn.

If you have a feeling there's a better way to do this than manually, you would be right: Vercel has a CLI tool
that [includes a `vercel alias` command](https://vercel.com/docs/cli/alias). Interestingly, this command doesn't seem to
make
a difference between Preview and Production environment aliases and doesn't require you to specify a branch - so not
only can you automate this process, going
through the CLI is actually easier. <span class="tooltip-toggle" aria-label="Aw! Not so hard you brute!">Pinch
me</span>.

```bash
vercel alias set [deployment-url] [custom-domain]
```

One last and **very valuable information** is that, while the Vercel docs heavily insist on the fact that you can use
your own domain as a custom alias (they even offer to purchase one through them - how convenient!), you can instead
create a
`.vercel.app` domain **for free**. While this is vaguely mentioned in the docs, I would argue this isn't super
clear.

## Vercel `repository_dispatch` events

Additionally, Vercel's GitHub integration docs include
a [Repository dispatch events](https://vercel.com/docs/git/vercel-for-github#repository-dispatch-events) section that
states the following:

> Vercel sends `repository_dispatch` events to GitHub when the status of your deployment changes. These events can
> trigger GitHub Actions [...].

That sounds nice. Now, could there be an event sent when a deployment to the Preview environment ends successfully, upon
which we could, say, call the Vercel CLI to create an alias? According to Vercel's [own list of
`repository_dispatch` events](https://github.com/vercel/repository-dispatch?tab=readme-ov-file#supported-events), yes:

```yaml
# Deployment has finished building and has automatically been promoted to production
- 'vercel.deployment.success'
```

I'll just point out that this description **isn't quite accurate** - the `vercel.deployment.success` event is emitted
upon
successful deployment to any environment, regardless of whether this deployment has been promoted to Production or not.

Vercel's events are published with an accompanying payload that looks like this:

```json
{
  "environment": "production",
  "git": {
    "ref": "main",
    "sha": "abcdef1234567890abcdef1234567890abcdef12",
    "shortSha": "abcdef1"
  },
  "id": "dpl_1234567890abcdefghijklmnopqrstuvwxyz",
  "project": {
    "id": "prj_abcdef1234567890abcdef1234567890",
    "name": "example-project"
  },
  "state": {
    "type": "pending"
  },
  "url": "https://example-project-abc123.vercel.app"
}
```

2 fields are particularly interesting to us:

* `environment` - we're interested in deployments to the `preview` environment, so we'll have to pay attention to this
  value
* `url` - this field will be populated with the preview deployment's URL, which we will need to create an alias via the
  Vercel CLI

So, we can trigger a GitHub Actions workflow when a deployment terminates successfully, and we can use the Vercel CLI to
create a free `.vercel.app` alias (aka custom domain) for the environment on which the deployment was made. Let's get
cracking.

## Update an alias on successful deployment to Preview

The following GitHub Actions workflow, once pushed to your default branch, will listen for `vercel.deoloyment.success`
events and, if such an event was emitted for a deployment to the Preview environment, will recreate alias
`{your-alias}` (which you will need to replace with your own alias - ideally one ending in `.vercel.app`, for reason$
mentioned earlier) for the
Preview deployment URL that Vercel generated.

{% raw %}

```yaml
name: Create Alias For Vercel Preview Deployment

env:
  VERCEL_ORG_ID: ${{ secrets.VERCEL_ORG_ID }}
  VERCEL_PROJECT_ID: ${{ secrets.VERCEL_PROJECT_ID }}
on:
  repository_dispatch:
    types:
      - 'vercel.deployment.success'
jobs:
  create-alias:
    if: github.event.client_payload.environment == 'preview'
    runs-on: ubuntu-latest
    steps:
      - name: Install Node.js
        uses: actions/setup-node@v3
        with:
          node-version: 18
      - uses: pnpm/action-setup@v2
        name: Install pnpm
        id: pnpm-install
        with:
          version: 7
          run_install: false
      - name: Install Vercel CLI
        run: pnpm add --global vercel@latest
      - name: Create Alias
        env:
          DEPLOYED_URL: ${{ github.event.client_payload.url }}
        run: |
          vercel alias rm {your-alias} --yes --token=${{ secrets.VERCEL_TOKEN }}
          vercel alias set $DEPLOYED_URL {your-alias} --token=${{ secrets.VERCEL_TOKEN }}
```

{% endraw %}

If you wish to use this workflow as-is, you'll need to do 3 things:

##### 1. Define the following 3 actions secrets on your GitHub project (Settings > Security > Secrets and variables > Actions > Repository Secrets):

* `VERCEL_ORG_ID`: known as **Team ID** these days on Vercel; can be found in your Vercel team's settings (by
  default your team is called `{your-vercel-username}s-projects`), under General > Team ID
* `VERCEL_PROJECT_ID`: can be found in your Vercel project's settings, under General > Project ID
* `VERCEL_TOKEN`: a Vercel personal token; if you don't already have one, you can generate one from the Vercel
  dashboard by clicking on your user icon in the top right > Account Settings > Tokens

![_config.yml]({{ site.baseurl
}}/images/articles/2025-9-11-Free-Fixed-URL-To-Latest-Vercel-Preview-With-GitHub-Actions/github_secrets.png)

##### 2. Replace `{your-alias}` with the URL you wish to use

* For example, `my-webapp-preview.vercel.app` (remember that an alias in `.vercel.app` can be used for free, as long as
  no
  one has claimed it first)

{% raw %}

```yaml
      ...
        - name: Create Alias
      env:
        DEPLOYED_URL: ${{ github.event.client_payload.url }}
      run: |
        - vercel alias rm {your-alias} --yes --token=${{ secrets.VERCEL_TOKEN }}
        + vercel alias rm my-webapp-preview.vercel.app --yes --token=${{ secrets.VERCEL_TOKEN }}
        - vercel alias set $DEPLOYED_URL {your-alias} --token=${{ secrets.VERCEL_TOKEN }}
        + vercel alias set $DEPLOYED_URL my-webapp-preview.vercel.app --token=${{ secrets.VERCEL_TOKEN }}
```

{% endraw %}

##### 3. manually create the alias that you chose in the previous step, either via the Vercel CLI or on the Vercel dashboard directly

* This is because I was lazy and didn't implement a check that the alias exists before running `vercel alias rm`
* This command fails with a non-zero return code if the alias doesn't exist - so this workflow will keep failing
  until the alias is created
    * If you're feeling devopsy today, you can have a look at the [`alias` command docs](https://vercel.com/docs/cli/alias) to see how to implement that
      check yourself!

To manually create an alias, you can:

* Via the Vercel CLI:
    * Find any valid Vercel URL for your webapp (any deployment, past or current, Preview or Production, will do)
    * Run the command `vercel alias set {any-deployment-url} {your-alias}`. For example:

```bash
vercel alias set my-web-application-git-fe-dfe98e7-corentindautremes-projects.vercel.app my-web-application-preview.vercel.app
```

* On the Vercel dashboard:
    * In your project's Settings, go to **Domains**
    * Click on the "**Add Domain**" button
    * Enter your alias and choose an environment (and a branch if you chose the Preview environment; stick to Production
      if you don't have any active branch at the moment, you'll override this alias next time you push a branch so it
      doesn't really matter)

![_config.yml]({{ site.baseurl
}}/images/articles/2025-9-11-Free-Fixed-URL-To-Latest-Vercel-Preview-With-GitHub-Actions/vercel_domains.png)

![_config.yml]({{ site.baseurl
}}/images/articles/2025-9-11-Free-Fixed-URL-To-Latest-Vercel-Preview-With-GitHub-Actions/vercel_add_domain.png)

That's it! Push a new branch eligible to Preview deployments, and check the Actions tab of your GitHub repository towards
the end of the Vercel deployment to verify that your workflow has properly run. If it has, the webapp built from your branch
should be accessible at your chosen alias, and said alias should be listed under the Domains of your deployment on
Vercel.

![_config.yml]({{ site.baseurl
}}/images/articles/2025-9-11-Free-Fixed-URL-To-Latest-Vercel-Preview-With-GitHub-Actions/vercel_preview_url.png)