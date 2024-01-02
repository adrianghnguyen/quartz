---
aliases:
  - planning out a software project
  - planning software project
  - how to plan a software project
tags:
  - advice
  - computer-science/software-engineering
  - advice
file-created: 2023-05-07
file-modified: 2023-09-02
note-type: general
description: 
linter-yaml-title-alias: Creating an initial plan for software project
---

# Creating an initial plan for software project

#status/postponed

---

%%Working with [[Tim Vieregge]] to understand my project on [[2023-05-07]]%%

## Problem statement

%%What are you trying to do? %%

Look for potential markers of popularity via metrics such as number of comments, activity, etc within /r/kdrama

- Avoid prescriptive statements, or things which might cause you to already for potential solutions.
- Keep it broad and general.
- The statement should be outcome focused

### Goals

%% What things will this software do? Very high level, keep it related to what you are trying to do. Since this might apply to personal projects, educational objectives might count.%%

- Create living ETL pipeline
- Clean unstructured data
- Create end-to-end coding project
- Compare if reddit comment activity correlates with Nielsen Korea viewership ratings
- To prepare for future website hosting analytics dashboard populated by data pipeline

Parking lot
- See if ChatGPT can be used in cleaning data?
- Learn how to perform sentiment analysis?
- How to host a website/web platform?

### Non-goals

%% Anything you want to remind yourself that you don't want to do. You don't need to fill this out at the beginning, you can just add to it as things come up. %%

- Hosting data

## Design

%%What's the thing you're building? All the major pieces and how they'll communicate
Some questions:

-   Where are you getting the data?
-   How does the data get between each part?
-   What are the major operations that each part will do?
%%

Most of the time, software can become complicated - so we need to think of the various 'big components' which will power the thing. In the analogy of a car, it would be the engine, seats, car frame, etc.

- **Script** to fetch reddit API data
- **ETL system** to orchestrate jobs
	- **Script** for cleaning data, will most likely be combined/dependent upon ETL system
	- **Script** to calculate metrics upon cleaned data
- **Database** to store cleaned data

^ The fact that the last statement is ambiguous means that more fundamental decomposition probably needs to be done. [[Decompose difficult problems into smaller parts|Break problems into small pieces.]] Repeat the process until it is digestible.

Advice: If you feel like you're getting lost in the weeds, sometimes just go and work on something which you think you can solve to get momentum/small victories.

## Rollout plan

%% How are you going to run this thing? What things need to be set up for this project to work? e.g. a linux pc, some data pipeline, a database server? %%

- May not be as important in terms of personal hobbies, at least for now
- It's useful to think in terms of physical resources or what needs to run the program.
- Avoid losing sight on the goal. Try and keep making progress.
- Try and avoid [[Do the thing instead of passive learning|analysis paralysis]]
- Avoid [[Perfectionism]] [[Good structure emerges organically|as good structure emerges organically]]
