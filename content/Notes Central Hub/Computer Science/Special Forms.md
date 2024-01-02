---
dg-publish: true
aliases: Special forms are exceptions of the general evaluation rule, special form, special forms
file-created: 2023-03-01
file-modified: 2023-05-05
tags: [computer-science]
linter-yaml-title-alias: Special forms are exceptions of the general evaluation rule
---

# Special forms are exceptions of the general evaluation rule

#status/wip

Related to [[Evaluating primitive expressions]]

---

Exceptions to the general evaluation rule are called *special forms*

- Each special form has its own evaluation rule ([[Expressions in programming]])
- The various kinds of expressions (each with its associated [[Evaluation Rule|evaluation rule]]) constitute the syntax of the [[Programming languages|programming language]]
	- `define` within lisp ([[Lisp as a programming language]]) is an example.

See also [[Lisp as a programming language]] to understand how it uses mainly general rules along with specialized rules to keep special forms to a minimum.

## List of special forms

- Operators such as + or -
- `if` and `or` (see [[Special forms  in conditional expressions]])
