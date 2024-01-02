---
aliases:
  - Playwright
tags:
  - computer-science/programming
  - computer-science/software-engineering
file-created: 2023-03-21
file-modified: 2023-09-02
note-type: general
description: 
linter-yaml-title-alias: Playwright
---

#status/postponed

# Playwright

## What is PlayWright?

It's a framework like selenium for E2E testing. The first step is to install it by running the command line install to Install playwright. Once it's installed, we can start a new javascript command then run another CLI line to open up a Chromium inspector. From there, you can generate the automation scripts by simply clicking and navigating as usual.

This will generate test code which we can review afterwards to see what it's trying to write out.

Browser -> Context -> Page

We can then paste the code into our test script file.

Main source :https://www.youtube.com/watch?v=wGr5rz8WGCE

### Cool playwright features

- Take screenshots at any steps of the testing processs
- Record video of the automation test
- Can run in headless mode by setting headless: false or removing it from the thing. This would allow to save on resources if human intervention isn't necessary

### Object hierarchy within playwright

Browser -> Context -> Page

### What is happening under the hood in this process?

1. Starts browser
2. Starts context which we can think of as a new environment instance for the inspector. 5 contexts = 5 different browsers envs. This would allow for independent but parallel testing.

## Installation steps

- Install package
- Configure repo
- Run inspection browser to generate test
- Review and place code in repo

## Basic documentation

- [Getting started - VS Code | Playwright](https://playwright.dev/docs/getting-started-vscode)
