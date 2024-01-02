---
dg-publish: true
aliases: Understanding the order in which arguments are evaluated or substituted, evaluation approach, substitution model, applicative order, normal order, applicative order evaluation, normal order evaluation, difference between applicative and normal order evaluation
file-created: 2023-02-28
file-modified: 2023-05-05
tags: [mathematics, mathematics, definition/difference, computer-science]
linter-yaml-title-alias: Understanding the order in which arguments are evaluated or substituted
---

# Understanding the order in which arguments are evaluated or substituted

#status/done

Related to [[Substitution model in computer science]]

---

## Illustrating the difference in evaluation methods

To illustrate the difference between the two evaluation methods, consider the following example expression:

`f(x) + g(x)`

Suppose the following:

- If x is equal to 2
- f(x) = x * 2
- while g(x) = x + 1, then:
Concept | Applicative order evaluation | Normal order evaluation
---| --- | ----
Technical explanation | would first evaluate x to 2, then evaluate f(x) to 4, and g(x) to 3, and finally add those two values to get 7 | substitute x into the function expressions first, resulting in (x \* 2) + (x + 1). Then, it would reduce that expression as much as possible, first by multiplying x by 2 to get 2 * 2, and then adding 1 to get 5. Finally, it would add those two values together to get 7.
ELI5 | If we think of it in terms of the math function, this method does f(x) and g(x) first by putting in x=2. Once it does the operands, it goes on to do the f(x) + g(x)| Expand f(x) with `x * 2` and expand g(x) with `x + 1` so it becomes `x * 2 + x +1` which results in `3x + 1`

## Applicative order evaluation

- Can be summarized as "Evaluate the arguments and then apply"
- Do the smallest inner units and substitution first.

> Applicative order evaluation involves **first evaluating** all the arguments of a function, and **then applying** the function to those arguments.

## Normal-order evaluation

- Can be summarized as "fully expand then reduce"
- Apply the top level, then proceed from there

> Normal order evaluation involves **substituting the arguments directly into the function expression**, and then reducing the resulting expression as much as possible before evaluating.
>
> In other words, normal order evaluation **delays** the evaluation of arguments **until they are needed**, and then applies the function to those unevaluated expressions.
