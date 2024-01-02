---
dg-publish: true
aliases: Compound procedures, procedure definition, compound procedure, compound operation
file-created: 2023-02-28
file-modified: 2023-05-05
tags: [computer-science]
linter-yaml-title-alias: Compound procedures
---

# Compound procedures

#status/done

Related to [[Structure and Interpretation of Computer Programs second edition by Harold Abelson Gerald Jay Sussman]]

---

## Procedure definitions as an abstraction technique

A compound operation can be given a name ([[Environments and names in computers]]) and then referred to as a unit, that is a *procedure definition*. That's something similar like in math giving a function…we encapsulate a concept through a formula.

Only powerful programming languages ([[Features of Powerful Programming Languages]]) are able to do this with their properties of definitions associating names with values as a means of abstraction.

> Compound procedures are used in exactly the same way as primitive procedures ([[Evaluating primitive expressions]]).
>
> Indeed, one could not tell by looking at the definition of sum-of-squares given above whether square was built into the interpreter, like + and *, or defined as a compound procedure.^[https://sarabander.github.io/sicp/html/1_002e1.xhtml#g_t1_002e1]

## General form of procedure definition

The general form of a procedure definition is `(define (⟨name⟩ ⟨formal parameters⟩) ⟨body⟩)`

the entire thing can be referred to as a *procedure*

- The `⟨name⟩` is a symbol to be associated with the procedure definition in the environment - aka assigning variable name to environment.
- The `⟨formal parameters⟩` are the names used within the body of the procedure to refer to the corresponding arguments of the procedure aka what are you using as your **function input**.
- The `⟨body⟩` is an expression that will yield the value of the procedure application when the formal parameters are replaced by the actual arguments to which the procedure is applied - **what do operations do you want done?**.
-  The `⟨name⟩` and the `⟨formal parameters⟩` are grouped within parentheses, just as they would be in an actual call to the procedure being defined - this is where the term **function call** comes from

## Squaring as an example of a compound procedure

We begin by examining how to express the idea of “squaring.” We might say, “To square something, multiply it by itself.” This is expressed in our language as:

![[Pasted image 20230228171708.png]]

Evaluating the definition creates this compound procedure and associates it with the name square.

### Connecting the terminology of a general form of procedure definition to the example

General procedure form concept | In the example | Explained further
---| --- |---
Procedure name | define (square x) | How we're going to refer to the concept of the procedure aka the *function call*
name | square | The function's name or the alias itself of the general procedure
formal parameter | x within the context of `(square x)` | what will be varying as we send it into the function
body | (* x x) | The operation to do within the function

See also [[Substitution model in computer science]]
