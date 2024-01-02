---
dg-publish: true
aliases: Lisp as a programming language, lisp, practical programming language, Lisp
file-created: 2023-02-27
file-modified: 2023-05-05
tags: [computer-science/programming, computer-science]
linter-yaml-title-alias: Lisp as a programming language
---

# Lisp as a programming language

#status/done

Related to [[Philosophy of Computer Science]]

---

## History of lisp

Lisp was invented in the late 1950s as a formalism for reasoning about the use of certain kinds of logical expressions, called recursion equations, as a model for computation.

Lisp, whose name is an acronym for LISt Processing, was designed to provide **symbol-manipulating capabilities** for attacking programming problems such as the symbolic differentiation and integration of algebraic expressions. It included for this purpose new data objects known as atoms and **lists**, which most strikingly set it apart from all other languages of the period.

One of its common dialects is *Scheme*.

## Why use lisp?

It contains unique features to understanding programming constructs, data structures and the linguistic features to implement them.

> Lisp descriptions of processes, called procedures, can themselves be represented and manipulated as Lisp data.
>
> The importance of this is that there are powerful program-design techniques that rely on the ability to blur the traditional distinction between “passive” data and “active” processes.
>
> As we shall discover, Lisp’s flexibility in handling procedures as data makes it one of the most convenient languages in existence for exploring these techniques. The ability to represent procedures as data also makes Lisp an excellent language for writing programs that must manipulate other programs as data, such as the interpreters and compilers that support computer languages. Above and beyond these considerations, programming in Lisp is great fun.^[https://sarabander.github.io/sicp/html/Chapter-1.xhtml#Chapter-1]

## Lisp is used in computer science curriculums

Course being in reference to [[Structure and Interpretation of Computer Programs second edition by Harold Abelson Gerald Jay Sussman]]

Lisp and Scheme are often taught in courses because it's easy to grasp with little emphasis on syntax - i.e. easy to write. I'm writing this within my notes so if in the future I search for my notes - this will explain where those programming languages come from.

> The syntactic structure of Lisp is reflected in its use of S-expressions and the uniformity of its syntax. This makes it easy to write and manipulate programs in Lisp, as well as to build tools for manipulating Lisp code. Additionally, the simplicity of Lisp's syntax makes it well-suited for developing domain-specific languages (DSLs) and for use in [[Artificial intelligence|artificial intelligence]] and [[Machine Learning|machine learning]] applications.^[ChatGPT]

Additional benefits:

- Focuses on modular thinking with decomposition as a thinking technique in order to develop large-scale systems.

See also [[Scheme as a programming language]]

## Personal usage of lisp

I've installed Lisp on my desktop computer using Portacle - all in one exe so I can use it in my studies of CS ([[Structure and Interpretation of Computer Programs second edition by Harold Abelson Gerald Jay Sussman]]).

### Evaluation rules within lisp

In comparison with most other programming languages, Lisp has a very simple syntax; that is, the evaluation rule for expressions can be described by a **simple general rule** together with **specialized rules** for a small number of *special forms*.
