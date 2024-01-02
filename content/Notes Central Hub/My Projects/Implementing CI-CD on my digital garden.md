---
dg-publish: true
aliases:
  - Implementing CI-CD on my digital garden
  - implementing CI/CD in my digital garden
  - implementing CI/CD on my blog
  - trying out CI/CD
  - CICD project
file-created: 2023-03-15
file-modified: 2023-05-17
tags:
  - my-projects
  - computer-science/programming
  - computer-science/software-engineering
note-type: project
linter-yaml-title-alias: Implementing CI-CD on my digital garden
difficulty: medium
description: Implement best practices for CI-CD on digital garden
progress: 
 - done
---

# Implementing CI-CD on my digital garden

## Basic project information

start: 2023-03-15
Related to [[Notes Central Hub/My Projects/Publishing my digital garden]]

### Summary, goals and objectives %%write overall description of project%%

I want to implement best practices for my [digital garden being hosted on Vercel](https://adrian-public-digital-garden.vercel.app/).  So what's happened recently, is that I would automatically publish some files. And sometimes the [[Context on My Vercel Publishing Issue|repo will not copy over properly]]. So if I implement some best practices, then I can automatically check to see if things become broken.

It's also an opportunity for me to learn some new software design principles or rather deployment practices. My blog is a safe testing environment for me to freely explore.

#### Objectives

- Implement website checks to ensure website is rendering properly
- Make sure navigation bar is working okay
- Ensure full clone of repo
- Ensure that links within the navigation bars are working
	- No dead links

### Project resources %%books, websites, etc. which were beneficial or are helping me out%%

- [[Continuous Integration and Deployment]]
- [Checkly](https://www.checklyhq.com/guides/) is already integrated in Vercel and I'll be using it for my [[Monitoring as code]]
- [A Complete Guide To Playwright Assertions](https://www.lambdatest.com/learning-hub/playwright-assertions)

%%

### Who can help?

%%

---

## Project diary and tasks

- [x] Research basic configuration process ✅ 2023-04-17
- [x] Configure necessary resources ✅ 2023-04-17
	- [x] Playwright ✅ 2023-04-17
	- [x] Checkly CLI ✅ 2023-04-17
	- [x] API key with Vercel ✅ 2023-04-17
- [x] Learn how Checkly works ✅ 2023-04-17
- [x] Configure basic tests ✅ 2023-05-17
- [x] Try out pipeline ✅ 2023-05-17
- [x] Do real user testing ✅ 2023-05-17
- [x] Try and break the pipeline to validate test ✅ 2023-05-17

- [[2023-03-15]]
	- Trying to understand what are the basic steps and components of what I need to do to implement
- [[2023-03-21]]
	- Research the basic workflow and wrote out my tasks
- [[2023-04-17]]
	- Needed to install [[Node.JS]] to have npm module. Seems to take a while to install - maybe it's big? This will allow me to use the PlayWright extension within [[Visual Studio Code|VS code]], my code editor and run E2E endpoint test generation within the built-in browser.
	- I needed to allow the [[Visual Studio Code|VS code editor]] to have script execution rights using the following command
	- ran `npminit playwright@latest` in order to install initiate my repo
	- Playwright basic VS code test tutorial video
		- Lots of basic commands in the testing explorer within VS code for the Playwright extension
		- [Getting started - VS Code | Playwright](https://playwright.dev/docs/getting-started-vscode)

### Possible user paths to test out

- home path
	- maps of content
		- recently published files
		- all available tags
	- Notes central hub
		- General notes page
			- https://adrian-public-digital-garden.vercel.app/202303171553
		- Computer Science
			- https://adrian-public-digital-garden.vercel.app/202303171550
	- Hobbies
		- Cycling
	- Projects
		- My projects
	- search bar
- no private files

### Test case scenarios

---

## Learned lessons

> [!faq] What went well? What went poorly? What can we do better?

Project-end-date:: [[2023-05-10]]

- I got to try out a new tool
- I learned how synthetic monitoring works
- Learned a bit more about how Playwright and Vercel interact

---

## Mentions

%%All linked notes associates to this file%%

```dataview
	LIST
	FROM [[]] AND !#folder AND !#admin AND !"Administrative"
```
