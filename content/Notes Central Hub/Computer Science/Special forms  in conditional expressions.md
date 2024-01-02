---
dg-publish: true
aliases: Special forms related to conditional expressions and predicates, if statement, or statement, boolean expression, case statement
file-created: 2023-03-01
file-modified: 2023-05-05
tags: [computer-science]
linter-yaml-title-alias: Special forms related to conditional expressions and predicates
---

# Special forms related to conditional expressions and predicates

#status/done

- Related to [[Conditional Expressions and Predicates]]
- [[Special Forms]]

---

## Special form - if

It's a special *restricted* type of conditional statement which can only be used when there are only **two cases** in case analysis.

`(if ⟨predicate⟩ ⟨consequent⟩ ⟨alternative⟩)`

```lisp
%% Uses special form of if%%
(define (abs x)
  (if (< x 0)
      (- x)
      x))
```

## Special forms of `and` and o`r`

- (and ⟨e₁⟩ … ⟨eₙ⟩)
	- everything must be true in the evaluation (left-right) otherwise return false
- (or ⟨e₁⟩ … ⟨eₙ⟩)
	- only one must be true in the valuation otherwise return false

> [!NOTE] `not` is considered an ordinary procedure
