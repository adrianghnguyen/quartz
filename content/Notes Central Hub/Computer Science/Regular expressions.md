---
dg-publish: true
aliases:
  - Regular expressions
  - regex
  - text
  - parsing
  - filtering
tags:
  - computer-science/programming
  - computer-science
file-created: 2023-02-15
file-modified: 2023-09-02
note-type: 
description: 
linter-yaml-title-alias: Regular expressions
---

# Regular expressions

#status/done

---

It's used to parse text and filter/select particular things through expressing patterns using its own form of syntax.

At this moment in time, I am using it to find out when I have bad strings in my [[Catching bad permalink string in Obsidian Publish|Obsidian publishing]].

[[Obsidian metadata management|Obsidian metadata management]]

I was messing around with regex to fix up my [[My personal knowledge management best practices|PKM vault]]. It's incredibly useful for mass editing text files, which is all that Obsidian is, since they're all based on markdown.

## Useful resources on RegEx

- Testing out Regex and can use it for debugging. [regex101: build, test, and debug regex](https://regex101.com/)
- [Python Regex Capturing Groups – PYnative](https://pynative.com/python-regex-capturing-groups/) <- explains how to break out a capture of a regex string into smaller sub components to manipulate
A good resource is to this website which allows debugging:

## Match groups

- Capturing things in parathesis allows us to re-used them in replacement or substitution functions using $1 etc.

![[Regular expressions-1.png]]
## Useful regex expressions

### Capturing date files

- Captures `[[YYYY-MM-DD]]`
	- `\[\[(\d{4}-\d{2}-\d{2})\]\]`

### Non-greedy capture

Aka finding things deeper into the line.

> The regex pattern `.*?` is used to match any sequence of characters (including no characters at all) in a non-greedy or lazy manner. Let's break down what `.*?` does:
>
> 1. `.*`: The `.` (dot) matches any character except for a newline character (`\n`). The `*` quantifier means "zero or more" of the preceding character or group, which, in this case, is the dot. So, `.*` matches zero or more characters.
>
> 2. `?` (Question Mark): The question mark immediately following the `*` makes the `*` quantifier non-greedy or lazy. This means that it will match as few characters as possible while still allowing the rest of the regex pattern to match.
>
> Here's how `.*?` behaves:
>
> - Without the `?`, `.*` would be greedy, matching as many characters as possible. For example, in the string "abcde", `.*` would match the entire string "abcde" because it's trying to maximize the number of characters matched.
>
> - With the `?`, `.*?` becomes non-greedy. It matches as few characters as possible while still allowing the remainder of the regex pattern to match. For example, in the string "abcde", `.*?` would match just "a" because it matches the minimum required to satisfy the rest of the pattern.
>
> The non-greedy behavior is especially useful when you want to capture the shortest possible substring that satisfies the overall regex pattern, such as in cases where you want to ignore leading text and match specific content within a larger string.
>
> In summary, `.*?` is a non-greedy quantifier that matches zero or more characters in the least greedy way possible.



