---
dg-publish: true
aliases: Computational objects are an entity that represents a value or a set of values, objects, oop, object-oriented programming, object names, set of values, what is a computational object
file-created: 2023-02-28
file-modified: 2023-06-17
tags: [environment, computer-science]
linter-yaml-title-alias: Computational objects are an entity that represents a value or a set of values
---

# Computational objects are an entity that represents a value or a set of values

#status/done

Related to [[Structure and Interpretation of Computer Programs second edition by Harold Abelson Gerald Jay Sussman]]

---

## Definition of computational objects

> In computer science, a computational object is an **entity that represents a value or a set of values**, and can be manipulated or operated on by a computer program. Computational objects can take many forms, depending on the programming language or paradigm being used.^[ ChatGPT]

- A **computational object** is represented by a name, which identifies a variable whose value is the object
- Values are associated with symbols within an [[Interpreters in programming|interpreter]]

> [!NOTE] Relating to it personally?
> It's kinda like saying I am Adrian (name), who is a person (object). Variable just refers to the fact that I can be flexible?

In [[Scheme as a programming language|scheme]], `define` is the simplest means of abstraction. It allows **names** to be used in compound operations (see [[Expressions in programming]]).

## Why do we use names to refer to computational objects?

- Computational objects can be very complicated in terms of structures and it would be hard to remember each individual components/details to form the whole.
	- You can think of it as [[Use concept handles to represent complex ideas|concept handles]] in terms of how it encapsulates a lot of atomic notes to represent a whole. When we say a [[Use concept handles to represent complex ideas|concept handle]], we refer to all the sub-ideas without needed to expound upon each one. We just 'get it' and retrieve it from memory.
- 'complex programs are constructed by building, step by step, computational objects of increasing complexity' which the interpreter abstracts for us by building each name-object associate incrementally^[https://sarabander.github.io/sicp/html/1_002e1.xhtml#g_t1_002e1]
	- Build atoms to build bigger molecules
	- It encourages incremental development and testing of programs, at least within the [[Lisp as a programming language|lisp]] paradigm which is just a bunch of strung together procedures

See also [[Environments and names in computers]]
