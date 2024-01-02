---
dg-publish: true
aliases: Conditional expressions and predicates, conditional expression, case analysis, predicate, if special form, special form
file-created: 2023-03-01
file-modified: 2023-05-05
tags: [computer-science]
linter-yaml-title-alias: Conditional expressions and predicates
---

# Conditional expressions and predicates

#status/done

Related to [[Structure and Interpretation of Computer Programs second edition by Harold Abelson Gerald Jay Sussman]]

---

In order to determine  if a number if positive, negative or zero and taking associated actions is not possible without the construct of *case analysis*. It can be used to test out scenarios during software development.

In Lisp ([[Lisp as a programming language]]), we use `cond` which is the short form of conditional, where it's written in this syntax:

```lisp
(define (abs x)
  (cond ((> x 0) x)
        ((= x 0) 0)
        ((< x 0) (- x))))
```

## General form of a conditional expression

```
(cond (⟨p₁⟩ ⟨e₁⟩)
      (⟨p₂⟩ ⟨e₂⟩)
      …
      (⟨pₙ⟩ ⟨eₙ⟩))
```

# The components of conditional expressions`

- **Clause**: the entire thing of p1 and e1
- Predicates: thing being evaluated for truth
- Consequent expression: what to return if predicate is evaluated to true

# Predicates

- **Predicate**: p1 and its friends aka the *[[Expressions in programming|expression]] being evaluated* ([[Expressions in programming]])
	- We evaluate each predicate in order from top to bottom.
	- We only pass onto the next predicate if the previous one was **not** true
	- Predicate is used for procedure that return Boolean values (true or false)
	- aka the antecedent
	- Can be used to describe
		- procedures that are Boolean
		- expressions which evaluate to Boolean values

## Details on predicates

**Primitive predicates** include <, =. > and logical composition operations such as *and, or, not*

- (and ⟨e₁⟩ … ⟨eₙ⟩)
	- everything must be true in the evaluation (left-right) otherwise return false
- (or ⟨e₁⟩ … ⟨eₙ⟩)
	- only one must be true in the valuation otherwise return false
- (not ⟨e⟩)
	- this expression is only true if `(e)` evaluates to *false*
	- Do the opposite

See also [[Special forms  in conditional expressions]]

# Consequent expression

- Consequent expression: the value to return if the predicate is evaluated to be *true*

## Example of absolute value

Absolute value is an example of a primitive procedure using conditional expressions ([[Evaluating primitive expressions]])

```lisp
%% One way of writing absolute-value procedure only using primitives%%
(define (abs x)
  (cond ((< x 0) (- x))
        (else x)))
```

# What is case analysis?

![[Administrative/File Attachments/Pasted image 20230301164402.png]]

Being able to do perform specific actions depending on the result through evaluation of a result.

> Case analysis refers to the process of examining different possible scenarios or cases in order to analyze how a program or algorithm will behave under each of them.
