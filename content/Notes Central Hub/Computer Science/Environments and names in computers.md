---
dg-publish: true
aliases: Environments allow interpreters to remember name-object pairs, variables, name-object pair, associations, global environment, computer environment, object context, environment context, environmental context, variable environment,
file-created: 2023-02-28
file-modified: 2023-05-05
tags: [definition, neuroscience/memory, computer-science]
linter-yaml-title-alias: Environments allow interpreters to remember name-object pairs
---

# Environments allow interpreters to remember name-object pairs

#status/done

Related to [[Computational object]]

---

## Creating local memory through assigning names within environments

In order for [[Interpreters in programming|interpreters]] need to have a form of memory (kinda like human [[Memory is processed information|memory]]!) in order to keep track of name-object pair associations.

[[Computational processes|Computations]] may require a multitude of combined environments.

> The general notion of the environment as providing a context in which [[Evaluating combinations|evaluation]] takes place will play an important role in our understanding of program execution (relationship to [[Interpreters in programming]] in how code is execute?).

### Use the special form to define variable names in the global environment context

This is often done through the [[Evaluating primitive expressions|special form]] of an [[Evaluation Rule]] like `define` in something like [[Lisp as a programming language|lisp]] to assign a name to a variable within an environment.

> [!NOTE] Reminder of what evaluation rules are
> Evaluation rules are how an interpreter does it computation processes and executes the code aka evaluating expressions (See [[Expressions in programming]])

This maybe be done within the *environment* or rather *global environment* (I'm assuming this is referring to the top-level layer/kinda like meta).
