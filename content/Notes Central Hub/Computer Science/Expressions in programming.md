---
dg-publish: true
aliases: evaluation rule, Expressions in programming, expression, expressions, expressions in programming, primitive, primitive cases, primitive expressions, fundamental expression, primitive expressionm evaluating expressions, definition of operator, definition of operand, compound operation
file-created: 2023-02-27
file-modified: 2023-05-05
tags: [definition, computer-science]
linter-yaml-title-alias: Expressions in programming
---

# Expressions in programming

#status/done

Related to [[Structure and Interpretation of Computer Programs second edition by Harold Abelson Gerald Jay Sussman]]

---

## A programming expression is a combination of values, operators or function calls to produce a resulting value

Expressions are a **fundamental concept** in programming languages and are used to **perform calculations, make decisions, and manipulate [[Data|data]]**.

A programming expression is a combination of one or more values, operators, and/or function calls that can be **evaluated (evaluation)**  to produce a new value. It's like things getting together to make a baby. The baby is the result of the programming expression.

An expression can be:

- as simple as printing a single value, such as a number or a string,
- can be more complex, involving multiple values and operators through combining it with a **primitive procedure**
	- such as + or * for adding and subtracting. Base arithmetic operations.

## Combinations also known as compound operations

> (+ 2.7 10)
> 12.7

- A **combination** is an expression is within parenthesis and contains a list of expressions - it's like the organizing of sub-expressions

### What is an operator?

- Leftmost "+" is called the *operator*
- What we're trying to do

### What are operands?

- Other elements are called *operands*
- What's being operated on

### What are arguments?

- *Arguments* are the values of the operands like the 2.7 and the 10

## Prefix notation

```lisp
(+ 21 35 12 7)
75

(* 25 4 12)
1200
```

Above is an example within [[Lisp as a programming language|lisp]].

Prefix notation, with the **operator** on the left of the expression, has several advantages despite being a bit different from the common math syntax.

- One of them is that it can accommodate procedures that may take an arbitrary number of arguments (21,35,12,7) to apply the entire operation
- Less ambiguity because the operator is always the leftmost element and the entire combination is delimited by the parentheses
- allows nesting (see example) which compilers know how to interpret without ambiguity in terms of what to do first, even with really complex examples

Even with complex expressions, the interpreter always operates in the same basic cycle: It reads an expression from the terminal, evaluates the expression, and prints the result. This mode of operation is often expressed by saying that the interpreter runs in a **read-eval-print loop**. Observe in particular that it is not necessary to explicitly instruct the interpreter to print the value of the expression.

### Nesting example

```lisp
(+ (* 3 5) (- 10 6))
19
```
