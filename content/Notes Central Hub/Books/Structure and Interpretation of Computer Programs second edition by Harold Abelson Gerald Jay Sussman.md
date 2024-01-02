---
dg-publish: true
aliases:
  - Structure and Interpretation of Computer Programs Second Edition by Harold Abelson Gerald Jay Sussman
  - introduction to CS
  - introduction to computer science
  - textbook on computer science
  - MIT textbook on CS
tags:
  - book
  - reference-material/learning
  - reference-material
  - computer-science
file-created: 2023-02-27
file-modified: 2023-09-21
note-type:
  - book
description: 
author:
  - Harold Abelson
  - Gerald Jay Sussman
cover: http://books.google.com/books/content?id=iL34DwAAQBAJ&printsec=frontcover&img=1&zoom=1&edge=curl&source=gbs_api
created: 2023-02-27 21:11:12
isbn: 262510871
linter-yaml-title-alias: Structure and Interpretation of Computer Programs Second Edition by Harold Abelson Gerald Jay Sussman
pages: 685
progress: [dropped]
published: 1996-07-25
publisher: MIT Press
title: Structure and Interpretation of Computer Programs, second edition
updated: 2023-02-27 21:11:12
---

![cover|150](http://books.google.com/books/content?id=iL34DwAAQBAJ&printsec=frontcover&img=1&zoom=1&edge=curl&source=gbs_api)

# Structure and Interpretation of Computer Programs Second Edition by Harold Abelson Gerald Jay Sussman

## About the Textbook

> [!NOTE] Book Summary
> Structure and Interpretation of Computer Programs is a computer science textbook by Massachusetts Institute of Technology professors Harold Abelson and Gerald Jay Sussman with Julie Sussman. The material in this book has been the basis of MIT’s entry-level computer science subject since 1980. It was critiqued on its obtuse approach [The Structure and Interpretation of the
> Computer Science Curriculum](https://www2.ccs.neu.edu/racket/pubs/jfp2004-fffk.pdf)
>
> They made their own book here: [[How to Design Programs second edition by Matthias Felleisen]]

### Key Themes Covered

- objects with state, concurrent programming, functional programming, lazy evaluation, and nondeterministic programming. We have included new sections on concurrency and nondeterminism

### Objective of the Textbook

- Introduce the concept of computer science ([[Map of Content/Computer Science]])
- For students with little to no formal training in computation
- establish the idea that a computer language is not just a way of getting a computer to perform operations but rather that it is a novel formal medium for expressing ideas about **methodology**
- Goal is to teach the philosophy of computer science over particular syntax or specifics

> [!quote] As written in the preface
> Our goal is that students who complete this subject should have a good feel for the elements of style and the aesthetics of programming. They should have command of the major techniques for controlling complexity in a large system. They should be capable of reading a 50-page-long program, if it is written in an exemplary style. They should know what not to read, and what they need not understand at any moment. They should feel secure about modifying a program, retaining the spirit and style of the original author.

### Exercises, Assignments and Projects

![[Administrative/File Attachments/Pasted image 20230301163654.png]]

[SICP-Solutions](http://community.schemewiki.org/?SICP-Solutions)

#### Textbook Projects

[Projects | Structure and Interpretation of Computer Programs | Electrical Engineering and Computer Science | MIT OpenCourseWare](https://ocw.mit.edu/courses/6-001-structure-and-interpretation-of-computer-programs-spring-2005/pages/projects/)
Section reading | Associated topic which to begin project | Project number
---|--- | ---
Section 1.1 |Scheme basics | Project 0
Section 1.3 |Higher order procedures | Project 1
Finished section 2.4 | Advanced data types | Project 2
Section 3.1 and 3.2 | Environment model | Project 3
Before beginning section 4 | Interpretation | Project 4
After section 5? | Geometric Folding Algorithms | Project 5

#### Exam Link

- Two quizzes

[Exams | Structure and Interpretation of Computer Programs | Electrical Engineering and Computer Science | MIT OpenCourseWare](https://ocw.mit.edu/courses/6-001-structure-and-interpretation-of-computer-programs-spring-2005/pages/exams/)

---

## Atomic Notes

> [!tip] Find MIT Open Courseware video lectures
> [Video Lectures | Structure and Interpretation of Computer Programs | Electrical Engineering and Computer Science | MIT OpenCourseWare](https://ocw.mit.edu/courses/6-001-structure-and-interpretation-of-computer-programs-spring-2005/video_galleries/video-lectures/)

- [x] Go in and backlink the notes and their appropriate concepts ✅ 2023-08-22

## Chapter 1: Building Abstractions with Procedures

- See also [[Philosophy of Computer Science]]
- See also [[Computational processes]]
- See also [[Traits of expert software engineers]]
- See also [[Programming languages]]
- See also [[Expressions in programming]]

## Naming and Environments in Computers

%%- [x] Need to make a summary for what I understood about naming and environments ✅ 2023-02-28%%

Names are how we refer to specific objects. Environments are the contexts in which names are assigned as variables (we call this definition - a special form further explored in [[Evaluating primitive expressions]]). Typically, there's a master environment which we can call the *global* [[Environments and names in computers|environment]].

- See also [[Computational object]]
- See also [[Evaluating combinations]]
- See also [[Compound procedures]]

See also [[Conditional Expressions and Predicates]]

---

## Additional Thoughts

### Thoughts and Reflections

- [[2023-02-27 Mon]]
	- I started reading this book as part of my journey to go towards [[Cognitive science|cognitive science]] which requires me to understand the fundamentals of computer science ([[Computer Science Education Hub]]).
- [[2023-03-03 Fri]]
	- It's interesting from a theoretical point but I don't feel a lot of connection with the content. It has exercises and projects but it's been critiqued as a learning method. It's also from the 80s where computer science education paradigms have changed better addressed by its successor. I need to reflect if this is analysis paralysis or am I punching above my weight class. I don't have an engineering or math background. If we think of it in terms of difficulty curves, this may be a bit too high for me.

	  Maybe I'll scan how to design programs to see if it covers similar content but in better context. There's value I think in finding something less dry. I also want something which makes me "good enough" rather than an expert. I just need to know enough so I can go back to connecting interdisciplinary knowledge and apply theories in computational form

### Related

- [[Map of Content/Computer Science]]
