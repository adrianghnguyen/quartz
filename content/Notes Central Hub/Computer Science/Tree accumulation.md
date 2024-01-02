---
dg-publish: true
aliases: Tree accumulation is a form of evaluation rule, hierarchy, hierarchical, treelike objects, tree-like objects
file-created: 2023-02-28
file-modified: 2023-05-05
tags: [computer-science]
linter-yaml-title-alias: Tree accumulation is a form of evaluation rule
---

# Tree accumulation is a form of evaluation rule

#status/done

Related to [[Evaluating combinations]]

---

The “percolate values upward” form of the [[Evaluating combinations|evaluation rule]] is an example of a general kind of [[Computational processes|process]] known as tree accumulation.

## Evaluation expression example

An example^[https://sarabander.github.io/sicp/html/1_002e1.xhtml#g_t1_002e1] of recursion with a hierarchical tree displays the idea of recursion can be seen in a deeply nested [[Evaluating combinations|combination]] such as

`(* (+ 2 (* 4 6)) (+ 3 5 7))`

![[Pasted image 20230228104403.png]]

We need to apply apply the rule 4 times in order to get the final result, just like BEDMAS. Start from the inside, go out until the top level. There are four layers.

In the example:

- Each [[Evaluating combinations|combination]] is a node
	- Each node has a branch with operators and operands coming out of it
- **Terminal nodes** (those with no branches) represent operators or numbers - aka the deepest layer…otherwise known as the ones which terminate the branch(duh!)
- Using the visual metaphor of the tree, it we can see evaluations as *percolating upward* from the **terminal nodes** to the **higher levels**
- If we keep applying the rule, aka digging deeper, we eventually hit rock-bottom where you need to do a [[Programming languages|primitive procedure]] rather than evaluate a combination
	- We evaluate the primitive expression like numerals, built-in operators and [[Computational object|object names]]
