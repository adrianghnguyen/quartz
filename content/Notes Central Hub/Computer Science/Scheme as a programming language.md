---
dg-publish: true
aliases: Scheme as a programming language, scheme, language related to lisp
file-created: 2023-02-28
file-modified: 2023-05-05
tags: [computer-science/programming, computer-science/programming, computer-science]
linter-yaml-title-alias: Scheme as a programming language
---

# Scheme as a programming language

#status/done

Related to [[Lisp as a programming language]]

---

In Common Lisp, a simple program would look something like the following:

```lisp
(defun fact (n)
     (if (< n 2)
         1
         (* n (fact (1- n)))))
```

In Scheme, the equivalent program would like like this:

```scheme
(define fact
     (lambda (n)
       (if (< n 2)
           1
         (* n (fact (- n 1))))))
```

Notice how scheme is a lot more simple in its syntax emphasis.

Scheme is often used in computer science curricula and programming language research, due to its ability to represent many programming abstractions with its simple primitives.

## Related

See also [FAQ: Lisp Frequently Asked Questions 1/7 [Monthly posting] - [1-1] What is the difference between Scheme and Common Lisp?](https://www.cs.cmu.edu/Groups/AI/html/faqs/lang/lisp/part1/faq-doc-2.html)
