---
dg-publish: 
aliases:
  - Optimal stopping
  - optimal stopping
  - knowing when to stop searching for more information
  - searching for more information
  - stopping point
  - stop searching for more information and simply make a decision
  - secretary problem
  - marriage problem
  - incomplete information
  - selecting the best option from a set of options
  - decision without complete information
  - 37% rule
tags: 
note-type:
  - general
description: 
file-created: 2023-11-15
file-modified: 2023-11-15
linter-yaml-title-alias: Optimal stopping
review:
---

# Optimal stopping

#status/postponed 

---

- [[Make informed decisions|Informed decision-making]]

Learned the concept from [[Algorithms to Live By by Brian Christian and Tom Griffiths|Algorithms to Live By by Brian Christian and Tom Griffiths]]. 

It helps us understand when we may need to stop searching for more information and simply make a decision - a [[Make quick and decisive actions|bias for action]]. It can serve as a [[Mental models make it easy for us to understand|mental model]] for dealing with incomplete information without understanding the size of the search space.

Humans have a tendency, perhaps due to anxiety and wishing to understand all consequences of their actions before making a decision. However, there's an optimal stopping point at which we have sufficient information to decide on our next course of action.

- See also [[Analysis paralysis|analysis paralysis]]
- [[explore-exploit trade off|Explore-exploit trade off]]

> [!ai]+ AI
>
> Optimal stopping, also known as the secretary problem or the marriage problem, is a mathematical problem that deals with decision-making and finding the best strategy to maximize the probability of selecting the best option from a set of options. It is often applied in scenarios where one needs to make a decision without having complete information about all available options.
> 
> The classic example of optimal stopping is the secretary problem. Imagine you have a set of potential applicants for a job position, and you want to select the best candidate. The applicants arrive in random order, and after each interview, you must decide whether to hire the candidate or move on to the next one. Once you reject an applicant, you cannot go back and choose them later. The goal is to select the best candidate while minimizing the chances of ending up with a suboptimal choice.
> 
> The optimal strategy in this scenario suggests that you should reject the first 37% (approximately) of applicants without hiring them and then choose the first candidate who is better than any of the previously interviewed ones. This strategy, known as "37% rule," provides a 37% chance of selecting the best applicant on average.
> 
> Optimal stopping can be applied in various situations such as job hiring, finding a life partner, purchasing a house, or even gambling. It aims to find an optimal threshold or stopping point that maximizes the chances of selecting the best option when faced with uncertainty.
> 
> Mathematically, optimal stopping problems are often solved using techniques from probability theory and decision theory. These problems can be quite complex, especially when there are additional constraints or uncertainties involved. However, they provide valuable insights into decision-making strategies and help in understanding how to make optimal choices when faced with limited information.

