---
dg-publish: true
dg-permalink: "20230202095116"
aliases: Debugging electronjs, debug
file-created: 2023-02-02
file-modified: 2023-05-05
tags: [computer-science/data/data-engineering, computer-science, computer-science/programming, theory/concept/framework, computer-science/programming, computer-science/programming]
linter-yaml-title-alias: Debugging electronjs
---

# Debugging electronjs

#status/done

---

## What is electronjs

- A framework which commonly powers by Chrome and Chromium engines
- Runs in JavaScript
- Ctrl+Shift+I opens up the inspector console which can help debug

## What the fuck am i doing today?

Trying to find out why the dg-garden plugin is fucking up.

I've identified that the `addPermalink` function doesn't seem to handle inputs which are non-strings gracefully. The input needs to be surrounded in quotes.

I'm starting to understand how to use the Chrome/ElectronJS console a bit better. After speaking with [[Justin Li]] they recommended that I set a breakpoint.

They also recommended I take a look at the following documentation on setting breakpoints within Chrome

https://developer.chrome.com/docs/devtools/javascript/breakpoints/

I started this because of [[Catching bad permalink string in Obsidian Publish]].

I can do a variable watch on the debugger

## Stack trace

Learning about the concept of a stack trace

https://www.sentinelone.com/blog/stack-trace-what-is-it-and-how-does-it-help-you-debug/

When there is an error, there's a trace of function calls up until that point hence, a stack trace. Typically operates on a Last-in First out basis (LIFO) - so stuff is printed top-down.

The first element in the list is the function that that threw the error. That's the culprit.

### Reading a stack trace

- Look at the first line, that's your culprit function. It will also print out the location of the exact line of code that's giving you the error.
- The other lines are all the leading calls to get to that point. So it's like an upside down waterfall.

#### Catch exceptions to solve third-party stack trace problems

One recommend is to use try-catch statements.

## Breakpoints

### What is a breakpoint

It's telling the computer to stop code execution at a certain point before it typically triggers an error which causes the program to stop.

Breakpoints are a more efficient way of debugging versus simply using console logs as it allows to fully inspect variables and their values.

## Types of breakpoints

See more here.

https://developer.chrome.com/docs/devtools/javascript/

https://developer.chrome.com/docs/devtools/javascript/breakpoints/ Use this?

## How to debug

1. Reproduce the bug
2. Look through your console and logs
3. Step through the code
4. Decompose the problem into individual blocks ([[Breakdown complex problems using First Principles Thinking]])
5. Inspect the values
6. Fix it
