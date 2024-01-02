---
dg-publish: true
aliases: Evaluating combinations is a form of expression evaluation, evaluation of combinations, combinations, combination, evaluation rule, evaluating
file-created: 2023-02-28
file-modified: 2023-05-05
tags: [mathematics, computer-science, mathematics, process]
linter-yaml-title-alias: Evaluating combinations is a form of expression evaluation
---

# Evaluating combinations is a form of expression evaluation

#status/done

Related to [[Structure and Interpretation of Computer Programs second edition by Harold Abelson Gerald Jay Sussman]]

---

## Definition of combination evaluation

Evaluating combinations - which are a form of [[Expressions in programming|expression]] -  requires us to do the following:

1. Evaluate the subexpressions of the combination - it's also called the **[[Evaluation Rule|evaluation rule]]**
	- Dig into the lower level before evaluating the top one - kinda like BEDMAS which is [[Recursion|recursion]]
2. Apply the [[Programming languages|procedure]] that is the value of the leftmost subexpression (the operator) to the arguments that are the values of the other subexpressions (the operands).

## Related

- See also [[Compound procedures]] to understand the general form of compound procedures which are used to define functions such as squaring(squa)
- See also [[Evaluating primitive expressions]]
