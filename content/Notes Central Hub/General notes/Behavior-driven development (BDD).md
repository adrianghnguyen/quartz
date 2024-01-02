---
aliases: Behavior-driven development (BDD)
tags: 
file-created: 2023-10-06
file-modified: 2023-10-06
note-type: general
description: null
linter-yaml-title-alias: Behavior-driven development (BDD)
dg-publish: true
---

# Behavior-driven development (BDD)

#status/done  #computer-science/software-engineering 

---

Related to [[Software testing]]

## Behavior-driven development (BDD)

![](https://wpblog.semaphoreci.com/wp-content/uploads/2022/05/bdd-08.jpg)

The difference under this [[Software testing|software testing]] paradigm is that it brings in the questions and assumptions of the users into the process at an earlier time. It requires one to write out behaviour tests before the code is written.

- [Power of Behaviour Driven Development: Building Better Software through natural language](https://www.linkedin.com/pulse/unlocking-power-bdd-building-better-software-through-natural-dhruvil/)

It can be challenging to create a company culture which truly adopts any type of software design methodologies such as agile or behavioural driven development. [Has anyone actually being able to truly implement BDD and TDD? : r/ExperiencedDevs](https://www.reddit.com/r/ExperiencedDevs/comments/nj7vhn/has_anyone_actually_being_able_to_truly_implement/) explains various reasons why they had success and how it at times doesn't.]

## Difficulties and challenges of BDD

Here are the core themes which lead to success in implementing a culture which uses [[Behavior-driven development (BDD)|Behavior-driven development (BDD)]]:
- Reality should drive processes, not the other way around. Work around how people actually work.
- The system should conform to the business users' needs
- There needs to be cultural buy-in
- Let people do what they do best. SDETs write the tests. Business users write their requirements.
- Engineers need to buy into the value of using tests to provide code coverage and ensure refactorability. All public functions should have *at least* a unit test attached. I think this is an [example case study at this person's startup](https://www.reddit.com/r/ExperiencedDevs/comments/nj7vhn/has_anyone_actually_being_able_to_truly_implement/gz7rxsv/) and how they implemented TDD.

[This response](https://www.reddit.com/r/QualityAssurance/comments/utq4yp/what_has_your_experience_been_with_bdd_test/i9fhjbz/) emphasizes that BDD is ultimately about collaboration between product owners and stakeholders to have [[Good communication requires effortful engagement|engaged communication]] early in the process of describing the behaviours which they wish to see in the software. A specific test should cover one functional behaviour. 

If you are describing unique behaviours then you should not be running into clashing function names.

## Advantages of behavioral-driven-development (BDD)

1. Improved communication: BDD tests are easily understood by both technical and non-technical team members, facilitating communication between developers, testers, and business stakeholders.
2. Focus on behavior: BDD emphasizes the behavior of the system instead of testing individual code units, ensuring that the system meets business requirements and provides value to users.
3. Collaboration: BDD promotes collaboration among team members, including developers, testers, and business stakeholders, enabling earlier issue detection and ensuring the system meets everyone's needs.
4. Test automation: BDD tests can be automated, enabling efficient testing of system changes, reducing manual testing efforts, and improving test accuracy and reliability.
5. Faster feedback: BDD's approach of writing tests before code provides developers with faster feedback about the impact of their changes, reducing debugging time and ensuring quicker delivery of changes

## Common BDD tools

> There are several tools available that can be helpful for Behavior-Driven Development (BDD), including:
>
> 1. Cucumber: A popular BDD testing tool that allows you to write tests in a natural language format.
> 2. Behave: A Python-based BDD testing tool that enables you to define tests in Gherkin syntax.
> 3. SpecFlow: A BDD testing tool for .NET developers that allows you to define tests in Gherkin syntax.
> 4. Jasmine: A JavaScript-based BDD testing tool that allows you to write tests in a behavior-driven style.
> 5. JBehave: A Java-based BDD testing tool that enables you to define tests in a plain text format.
> 6. Robot Framework: A Python-based testing framework that supports both BDD and keyword-driven testing.

## Gherkin for BDD

It can be useful for programmers, testers as well as product owners in terms of being a common language for BDD  as a domain specific language called [Gherkin](https://cucumber.io/docs/gherkin/)of the team to understand the expected behaviour of the code even by non-technical/business users.  We can write out the specific behaviours needed in this specific language which can be well understood by variety of stakeholders.

```gherkin
Given{Condition}

When{something happens}

Then{see results}
```

```gherkin
# Example of SpecFlow BDD feature case
Feature: Calculator
 
Calculator for adding two numbers
 
@mytag
Scenario: Add two numbers
Add two numbers with the calculator
Given I have entered <First> into the calculator
And I have entered <Second> into the calculator
 
When I press add
Then the result should be <Result> on the screen
Examples:
| First | Second | Result |
| 50    | 70     | 120    |
| 30    | 40     | 70     |
| 60    | 30     | 90     |
```