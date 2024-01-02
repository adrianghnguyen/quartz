---
dg-publish: true
aliases: Substitution model for procedure application, substitution model, substitution, sub model
file-created: 2023-02-28
file-modified: 2023-05-05
tags: [computer-science/programming, computer-science]
linter-yaml-title-alias: Substitution model for procedure application
---

# Substitution model for procedure application

#status/done

Related to [[Compound procedures]] and [[Procedure Application in Computer Science]]

---

## Definition of the substitution model

> [!NOTE] Subway - eat fresh?

To evaluate compound procedures, we do it the same way we do in in primitive procedures ([[Evaluating primitive expressions]]). We go down and evaluate until the lowest level (like in [[Tree accumulation]]) in a [[Recursion|recursive]] manner to retrieve the appropriate primitive procedure and how it was defined.

> We can assume that the mechanism for applying primitive procedures to arguments is built into the interpreter. To apply a compound procedure to arguments, **evaluate the body of the procedure with each formal parameter replaced by the corresponding argument**.

From a higher level function, we'll sub in the lower ones. Kinda like replace x with whatever x represents. All the way down! Cnce we've reached the primitive level, then we go and evaluate back up. This is called the **substitution model** for [[Procedure Application in Computer Science|procedure application]].

See also [[The map is not the territory]] to understand why we use this framework to understand the evaluation of compound procedures. This mental model doesn't hold when things become more complicated - but that's okay for now.

### Example of the substitution model process

The problem **reduces** to the evaluation of a [[Evaluating combinations|combination]] with two operands and an operator sum-of-squares.

```lisp
(f 5)
(sum-of-squares (+ a 1) (* a 2)) %%Retrieve the body of f%%
(sum-of-squares (+ 5 1) (* 5 2)) %%Replace the formal parameter a by the argument 5%%
```

If we think of it as a tree, it creates three sub-problems:

1. We must evaluate the operator to get the procedure `sum of square` to be applied to the *following two operands*
2. we must evaluate the operand -> `(+ 5 1)` produces 6
3. we must evaluate the operand -> `(* 5 2)` produces 10

```lisp
(+ (square 6) (square 10)) %% After evaluating each sub-problem%%
(+ (* 6 6) (* 10 10)) %% Applied definition of square%%
(+ 36 100) %% Reduced to multiplication %%
136 %% Final result %%
```

## Applicative order versus normal order

According to the [[Evaluation Rule|evaluation rule]], we need to go in a recursive manner to evaluate the operators and operands (evaluating expression in [[Expressions in programming]])

There are two main approaches:

- applicative order evaluation
- normal-order evaluation aka "fully expand and then reduce"

See also [[Applicative and Normal Order Evaluation]] to see it elaborated.

## Related
