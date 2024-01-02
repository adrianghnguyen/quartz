---
dg-publish: true
aliases: Difference between Function and Processes, functions and processes, processes and functions, function cake metaphor
file-created: 2023-03-12
file-modified: 2023-05-05
tags: [definition/difference, theory/concept, computer-science]
linter-yaml-title-alias: Difference between function and process
---

# Difference between function and process

#status/done

Related to [[Cognition aka the mental processes involved in understanding and processing interactions in the world]]

---

## Functions and processes

In simple terms, a process is a **series of steps** that are taken to achieve a specific goal, while a function is a specific task or operations (you can think of it as a block of code) that performs a specific task within a program.

See also [[Functions in programming]]

## Eli5 of function vs processes as making a cake metaphor

Think of a process as a recipe for making a cake. The recipe outlines the series of steps that must be taken in order to bake the cake, from mixing the ingredients to putting it in the oven to bake. Each step is necessary for achieving the final goal of having a fully baked cake.

The exact task of putting the batter in the oven and setting it to a specific temperature is the equivalent of a **function**.

### Cake programming metaphor

Here's an example of how we could write a function in python to bake a cake:

```python
def bake_cake(ingredients):
  mix_ingredients(ingredients)
  pour_batter()
  preheat_oven()
  bake_cake()
  cool_cake()
```

In this function, we take in the ingredients for baking the cake as input and then call other functions like mix_ingredients(), pour_batter(), preheat_oven(), bake_cake() and cool_cake() to perform different tasks necessary for baking the cake.
