---
aliases:
  - Resource based decision-making for scalability
tags:
  - decision
  - knowledge
  - engineering/infrastructure
  - design
  - reference-material
file-created: 2023-02-02
file-modified: 2023-09-02
note-type: general
description: 
linter-yaml-title-alias: Resource based decision-making for scalability
source:
  - "https://notes.andymatuschak.org/About_these_notes?stackedNotes=z2kr7QrJczqYyfwLFcv1FLEUMdVTsgfYSdFXA"
---

#status/postponed

---

# Resource based decision-making for scalability

> [!Warning] Reference note
> This was not written by me. It is included within my notes as I feel that it would be very valuable to in order to build base knowledge and references.
>
> The original source can be found here: **https://notes.andymatuschak.org/About_these_notes?stackedNotes=z2kr7QrJczqYyfwLFcv1FLEUMdVTsgfYSdFXA**

## My thoughts and reflections

Elaborate on this.

What happens when you try to create too many connections? What is the burden of trying to spread your resources too thin? What if you applied the wrong mental model and need to course correct. You need a certain level of flexibility to respond to changes.

Making decisions (choices, thinking) involve trade-offs (opportunity cost) so by limiting your need to make decisions - by delegating, reducing cognitive overhead, leveraging existing decision frameworks, you can devote more time to thinking about what matters (deep work)???? How does this relate?

So how do you grow and maintain adaptability?

What are the best ways of spending your resources in order to grow sustainable over a long period of time?

He specifically talks about **system iteration**. From what we know, the key to growth is the ability to go through faster improvement cycles as from what we can observe, evolutionary competitive advantage occurs with faster reinforcement cycles ([[Feedback loop]]) which is how we can improve ( [[Continuous feedback leads to change]])

What happens when you try to go through decision cycles too quickly? You fall prey to cognitive biases ([[Brains are biased by nature]])and fail to gain [[Develop situational awareness to understand the environment|situational awareness]] ([[OODA Loop]])

### Related

---

# Original article title: premature scaling can stunt system iteration

Particularly in Silicon Valley, when one has a prototype or an inkling that works well, the temptation is to scale it out. Make it work for more people and more use cases, turn it into a platform, make the graphs go up and to the right, etc. This is obviously a powerful playbook, but it should be deployed with careful timing because it tends to freeze the conceptual architecture of the system.

## Why

General infrastructure simply takes time to build. You have to carefully design interfaces, write documentation and tests, and make sure that your systems will handle load. All of that is rival with experimentation, and not just because it takes time to build: it also makes the system much more rigid.

Once you have lots of users with lots of use cases, it’s more difficult to change anything or to pursue radical experiments. You’ve got to make sure you don’t break things for people or else carefully communicate and manage change.

Those same varied users simply consume a great deal of time day-to-day: a fault which occurs for 1% of people will present no real problem in a small prototype, but it’ll be high-priority when you have 100k users.

Once this playbook becomes the primary goal, your incentives change: your goal will naturally become making the graphs go up, rather than answering fundamental questions about your system (contra [Focus on power over scale for transformative system design](https://notes.andymatuschak.org/z5pvC3U6Lt9EKPYPZ3PHUnrpu8QUN79GirjAJ)).

## On remaining small

One huge advantage to scaling up is that you’ll get far more feedback for your [Insight through making](https://notes.andymatuschak.org/z7YyAp683VNbTmDG4hx9QFpf5urwxZJpsycS6) process. It’s true that [Effective system design requires insights drawn from serious contexts of use](https://notes.andymatuschak.org/z3H98n8DGZmu8XArqHZVsckyWvbTe8wK4kAt2), but it’s possible to create small-scale serious contexts of use which will allow you to answer many core questions about your system. Indeed: technologists often instinctively scale their systems to increase the chances that they’ll get powerful feedback from serious users, but that’s quite a stochastic approach. You can accomplish that goal by carefully structuring your prototyping process. This may be better in the end because [Insight through making prefers bricolage to big design up front](https://notes.andymatuschak.org/z7Ldzn94FibghJBEG9hAebu8LMNV7NVBFvsfg)

Eventually, of course, you’ll need to generalize the system to answer certain questions, but at least in terms of research outcomes, it’s best to make scaling _follow_ the need expressed by those questions. In that sense, it’s an instrumental end, not an ultimate end.
