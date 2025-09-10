---
layout: post
title: GitHub badges without third-party services nor GitHub pages
---

Who doesn't want shiny badges to show off their coverage stats on their brand new side project? I, for one, did - but I
didn't want to rely on a third-party badge service, nor did I want to setup, like some suggest online, GitHub Pages on
my repo for this sole goal. But, with SVG and a bit of GitHub Actions magic, neither of these is needed!

<!--more-->

![_config.yml]({{ site.baseurl
}}/images/articles/2025-9-9-GitHub-Badges-Without-Third-Party-Services-Nor-GitHub-Pages/badges_example.png)

_The above badges on the readme of my [Transit Planner](https://github.com/corentindautreme/transit-planner) side
project always display the current coverage data for my main branch_

The main idea behind this is to have SVG templates for your badges stored somewhere on GitHub (for example, on your
repo) that you can duplicate and edit to update a placeholder that you included in your template. You can then embed the
populated template anywhere you want using an `img` tag that points to the raw URL of the SVG. And yes, GitHub's
markdown does support `img` tags!

<div style="text-align: center">
  <img src="https://raw.githubusercontent.com/corentindautreme/transit-planner/198931e50c3c15b252ea3367ec77951544ff2d8e/_templates/coverage/global.svg"/> => <img src="https://raw.githubusercontent.com/corentindautreme/transit-planner/198931e50c3c15b252ea3367ec77951544ff2d8e/coverage/global.svg"/>
</div>

I personally chose to keep my badges and their templates on a dedicated branch aptly named (you'll never guess 🥁)
`badges`, mainly to keep the commit history of my `main` branch clean.

```_
.
└── _templates
│   └── coverage
│       └── branch.svg
│       └── line.svg
└── coverage
    └── branch.svg
    └── line.svg
```

_I decided to group my badges by category. I only have coverage badges at the moment, so a `coverage/` directory
contains the SVG badges, while a `coverage/` directory under `_templates/` contains the templates._

All that's left to do is to write some code to take care of the template copy and population. You could plug a GitHub
Actions workflow that leverages on GitHub's `checkout` action to switch to the branch that contains your badges, and on
built-in bash tools like `sed`:

```yaml
  - name: Checkout 'badges'
    uses: actions/checkout@v4
    with:
      ref: badges
  - name: Generate badges
    run: |
      cp -r _templates/coverage/. coverage/
      cd coverage/
      sed -i -e "s/__VAL__/<line coverage value>/g" line.svg
      sed -i -e "s/__VAL__/<branch coverage value>/g" branch.svg
```

[Here's a full GitHub Actions workflow](https://github.com/corentindautreme/transit-planner/blob/ee5a4c6de09d1def8484ef894e52bb8a4def1bd1/.github/workflows/coverage-badges.yml)
that generates coverage badges for a Node.js project. It

* extracts the global coverage stats of a Node.js project from a `nyc` JSON report (generated upon calling the `test`
  command) and saves them to an environment variable
* checks out the `badges` branch of the repo
* copies the templates of the coverage SVG badges
* replaces the `__VAL__` placeholder in each copied template with the coverage value (line or branch)
* commits and pushes the new badges to the `badges` branch