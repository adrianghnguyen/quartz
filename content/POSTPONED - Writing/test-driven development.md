---
dg-publish: 
aliases:
  - test-driven development
  - TDD
  - test-driven development (TDD)
tags: 
file-created: 2023-10-06
file-modified: 2023-10-06
note-type:
  - general
description: 
linter-yaml-title-alias: test-driven development
review:
---

# Test-driven development

#status/postponed 

---

It's one of the software paradigms used in [[Software testing|software testing]] and is a predecessor framework to [[Behavior-driven development (BDD)|Behavior-driven development (BDD)]]. Learn more at [What Is Unit Testing? | SmartBear](https://smartbear.com/learn/automated-testing/what-is-unit-testing/).

> Test Driven Development, or TDD, is a code design technique where the programmer writes a test before any production code, and then writes the code that will make that test pass. The idea is that with a tiny bit of assurance from that initial test, the programmer can feel free to refactor and refactor some more to get the cleanest code they know how to write. The idea is simple, but like most simple things, the execution is hard. TDD requires a completely different mind set from what most people are used to and the tenacity to deal with a learning curve that may slow you down at first.

It's creating atomic unit tests which can test individual functions and is written in parallel as a function is finished up. It follows the assumption that the programmer who wrote the code knows how the initial test should be set up and under which conditions it should operate. 

The test should be small enough to be independent and not cross systems. I assume that this is in order to reduce knock-on effects by other systems and to keep the tests simple which make them easier to maintain. Otherwise, one would need to maintain the whole dependency in order to test a function.

At this time, it's something that's still difficult to be adopted by software teams and is entire standard procedure without deliberate organizational effort to instill a culture of TDD.

Long story short:
- Test your code often with small atomic tests
- Keep your tests bite-sized and avoid crossing systems where possible
- Instilling this discipline of software testing requires discipline