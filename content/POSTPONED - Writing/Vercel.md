---
aliases:
  - Vercel allows deployment of web projects and websites
  - Vercel
  - cloud platform for static websites
  - cloud platform for serverless functions
  - serverless functions
  - deploy websites
tags:
  - engineering/infrastructure
  - computer-science/software-engineering
  - computer-science/software-engineering
note-type: general
description: 
file-created: 2023-03-15
file-modified: 2023-12-04
linter-yaml-title-alias: Vercel allows deployment of web projects and websites
---

# Vercel allows deployment of web projects and websites

#status/wip

Related to [[Monitoring as code]]

---

> [!ai] AI
>
> Vercel is a cloud platform for static websites and serverless functions. It provides a fast and easy way to deploy websites, APIs, and other web projects with high performance and reliability. Vercel supports a wide range of popular frameworks and programming languages, including React, Next.js, Vue.js, Angular, Gatsby, and more. It also offers a suite of developer tools such as real-time collaboration, preview URLs, automatic SSL certificates, and integrations with popular version control systems like Git. Vercel is used by developers and businesses worldwide to build modern web applications that scale seamlessly.

## Digital garden deployment workflow

It's used within [[Notes Central Hub/My Projects/Publishing my digital garden|my digital garden]] to automatically deploy my Obsidian writing notes over to an online website. It works by coping my private github repo for my notes by parsing for a publish attribute on the file. Then it clones the repo into the digital garden repo which triggers a build command over to the Vercel platform. This renders out all the changed files as new static pages.

[What does Vercel do? – Vercel](https://vercel.com/blog/what-is-vercel)

Build step
- [Projects Overview | Vercel Docs](https://vercel.com/docs/projects/overview#ignored-build-step)

## Ignoring build steps

[Feature request: Ignored branches for deploy previews · Issue #3166 · vercel/vercel · GitHub](https://github.com/vercel/vercel/issues/3166)

```js
[ $VERCEL_GIT_COMMIT_REF != "preview" ] && [ $VERCEL_GIT_COMMIT_REF != "production" ]
```
Supposedly this command in the `ignore build step` will help prevent triggering [[Github|git]] deployments to cause new builds to be triggered. It restricts it only to branches with the name `preview` or `production`

The problem I was trying to solve is that my Obsidian digital garden plugin publishes a lot of commits. I plan to squash these into a pull request called `deployment`. The issue is that the way Vercel seems to be structured, as opposed to Netlify is that there's no opt-in build setting.

It needs to be structured at the project level, which means builds are triggered then cancelled, costing resources.
