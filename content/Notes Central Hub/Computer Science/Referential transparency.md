---
aliases: Referential transparency, no change in output, subsitute
file-created: 2023-03-19
file-modified: 2023-05-05
tags: [computer-science, theory/concept, mathematics, linguistics]
linter-yaml-title-alias: Referential transparency
---

# Referential transparency

#status/wip

Related to [[Data Warehouse]]

---

## Referential transparency in computer science

If you can replace the input with something *equivalent* without changing the output of the [[Functions|function]]. Are you able to use a substitute without changing the outcome?

> In [computer science](https://en.wikipedia.org/wiki/Computer_science "Computer science"), **referential transparency** and **referential opacity** are properties of parts of [computer programs](https://en.wikipedia.org/wiki/Computer_program "Computer program"). An [expression](https://en.wikipedia.org/wiki/Expression_(programming) "Expression (programming)") is called _referentially transparent_ if it can be [replaced](https://en.wikipedia.org/wiki/Rewriting "Rewriting") with its corresponding value (and vice-versa) without changing the program's behavior.[[1]](https://en.wikipedia.org/wiki/Referential_transparency#cite_note-1) This requires that the expression be [pure](https://en.wikipedia.org/wiki/Pure_function "Pure function") – its value must be the same for the same inputs and its evaluation must have no [side effects](https://en.wikipedia.org/wiki/Side_effect_(computer_science) "Side effect (computer science)"). An expression that is not referentially transparent is called **referentially opaque**.
> \- Wikipedia

## Linguistics example for referential transparency

> A context in a sentence is "referentially transparent" if replacing a term in that context by another term that _refers to the same entity_ doesn't alter the meaning. For example
>
> The Scottish Parliament meets in the capital of Scotland.
>
> means the same as
>
> The Scottish Parliament meets in Edinburgh.
>
> So the context "The Scottish Parliament meets in …" is a referentially transparent context. We can replace "the capital of Scotland" with "Edinburgh" without altering the meaning. To put another way, the context only cares about what the term refers to and nothing else. That is the sense in which the context is "referentially transparent."
>
> "Edinburgh has been the capital of Scotland since 1999." <- this is not referentially transparent
>
> ^[https://stackoverflow.com/questions/210835/what-is-referential-transparency]
