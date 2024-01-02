---
dg-publish: true
aliases: primitive procedure, Evaluating primitive cases in programming, primitive cases, primitive expression, special form, if special form, if statement
file-created: 2023-02-28
file-modified: 2023-05-05
tags: [computer-science]
linter-yaml-title-alias: Evaluating primitive cases in programming
---

# Evaluating primitive cases in programming

#status/done

Related to [[Evaluating combinations]]

---

Remember that primitive cases as explained within [[Expressions in programming|Expressions in Programming]] are the fundamental blocks of [[Programming languages|procedures]].

## The three rules of evaluation in computer programming

We begin by [[Evaluating combinations|evaluating]] the following rules:

1. the values of **numerals** are the numbers that they name ([[Computational object]]),
2. the values of **built-in operators** are the machine instruction sequences that carry out the corresponding operations ([[Expressions in programming]]), and
3. the values of **other names** are the objects associated with those names in the [[Environments and names in computers|environment]].

> [!NOTE] It's all coming together baby
> Notice how they all build upon each other? We apply operators to the numerals. Other names are built out of operators and the fundamental numerals.

- See also [[Tree accumulation]] for an example of this [[Evaluating combinations|evaluation rule]] in process.
- See also [[Special Forms]]

## Operators are a special exception of environment names

> We may regard the **second rule** as a **special case of the third one** by stipulating that symbols such as + and * are also included in the global environment ([[Environments and names in computers]]), and are associated with the sequences of machine instructions (See procedures in [[Programming languages]]) that are their “values.” The key point to notice is the role of the [[Environments and names in computers|environment]] in determining the meaning of the symbols in expressions.^[https://sarabander.github.io/sicp/html/1_002e1.xhtml#g_t1_002e1]

### Example within lisp

> [!NOTE] Illustrated within Lisp
> In an interactive language such as Lisp, it is meaningless to speak of the value of an expression such as (+ x 1) without specifying any information about the **environment that would provide a meaning for the symbol x** (or even for the symbol +)
>
> \-[Evaluating Combinations](https://sarabander.github.io/sicp/html/1_002e1.xhtml#g_t1_002e1)

> Notice that the evaluation rule given above does not handle definitions. For instance, evaluating (define x 3) does not apply define to two arguments, one of which is the value of the symbol x and the other of which is 3, since the purpose of the define is precisely to associate x with a value. (That is, (define x 3) is not a combination.)
