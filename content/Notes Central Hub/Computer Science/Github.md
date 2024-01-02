---
dg-publish: true
aliases: file version control, git, GitHub, github, git, version control system, versioning, file versioning
file-created: 2023-01-30
file-modified: 2023-07-06
tags: [computer-science, computer-science/data/data-engineering, computer-science/software-engineering, productivity, computer-science/software-engineering]
linter-yaml-title-alias: Git allows you to unscrew yourself when you mess up
---

#status/done

# Git allows you to unscrew yourself when you mess up

## What is git?

> Git is a distributed version control system used for software development. It was created by Linus Torvalds in 2005 to manage the development of the Linux kernel. Git allows multiple developers to collaborate on a project and keep track of changes made to the codebase over time. It enables developers to work on different branches of the codebase and merge their changes together seamlessly. Git also has robust features for tracking changes, managing conflicts, and restoring previous versions of files.

Often times, we work on files and need to go back and retrieve an older copy. What happens when you've deleted the file by accident? Or you realized that you need something from the version saved 3 months ago? That's why this kind of tool was made. It allows you to recover revisions and manage such file conflicts.

### Git data model

- [Git Data Model | Astah in 5min](https://astahblog.com/2015/09/08/git-data-model/)
- [Git cheatsheet and data model](http://ndpsoftware.com/git-cheatsheet.html#loc=index)

## Branches

Branches in Git are used to isolate work, experiment with new features, develop bug fixes, and collaborate with other team members. They're like a development snapshot which is used to merge into the main 'tree'. This allows you to separate out the development in little mini ecosystems.

I'm currently using Git for managing my Obsidian repo ([[Why I write in Obsidian]]) and it's saved my butt a few times in terms of being able to recover files or from mistakes.

### Why use branches in development?

Here are some reasons why branches are useful in Git:

> 1. Isolating work: Branches allow developers to work on multiple features or bug fixes simultaneously without affecting the main codebase. This makes it easier to test and deploy changes.
>
> 2. Experimenting: Branches can be used to test new features or ideas without affecting the main codebase. Developers can create a branch, make changes, and experiment without worrying about breaking the code.
>
> 3. Bug fixing: When a bug is found in the main codebase, developers can create a branch to fix the bug without affecting other parts of the code.
>
> 4. Collaboration: Branches allow multiple developers to work on different parts of the same project simultaneously. They can each create their own branch and collaborate on changes before merging them back into the main codebase.
>
> 5. Version control: Branches provide a way to keep track of different versions of the same codebase. This makes it easier for developers to roll back changes if necessary or compare different versions of the code.
>
> Overall, branches in Git provide a flexible and powerful way for developers to manage their work and collaborate effectively on projects.

### Delete your branches after merging into the main branch

[git - Should I delete a branch after merging it? - Stack Overflow](https://stackoverflow.com/questions/10765321/should-i-delete-a-branch-after-merging-it)

> There's no problem in deleting branches that have been merged in. All the commits are still available in the history, and even in the GitHub interface, they will still show up (see, e.g., [this PR](https://github.com/DanielStutzbach/blist/pull/40) which refers to a fork that I've deleted after the PR got accepted).

## What is staging?

Staging is the process of preparing files or changes to be committed to a version control system. It involves selecting and grouping changes, reviewing them for accuracy and completeness, and ensuring they are ready to be shared with others on the team.

Staging also allows developers to experiment with different changes and configurations before committing them to the main branch of a project. This helps prevent errors and conflicts that can arise when multiple people are working on the same code base simultaneously.

## Resolving merge conflicts

[[2023-01-28]] I ran into the problem of having a conflicting file. All I had to do was go into the resolving conflict editor on github and choose if I want to keep the incoming branch or the outgoing one. Just delete what you don't want to keep and hit resolve conflicts. I learned something new! Kinda cool I get more experience with Git as a result of publishing my digital garden ([[Share your journey publicly]]).

## Pull requests

### Pull requests in git

> [!ai]+ AI
>
> Pull requests in git are a way to propose changes to a repository on GitHub. They allow developers to submit their changes to a branch in the repository and request that those changes be reviewed and merged into the main branch.
> To create a pull request, a developer first needs to fork the repository they want to contribute to. This creates a copy of the repository under their own GitHub account. They can then clone this forked repository onto their local machine and make any desired changes.
> Once the changes are made, the developer can commit them to their local branch and push the changes back to their forked repository on GitHub. From there, they can open a pull request by clicking the "New pull request" button on the original repository's page.
> In the pull request, developers can provide a summary of the changes they made and any additional context or information. They can also choose specific branches for comparison and choose reviewers who will be notified to review the changes.
> Reviewers can leave comments on specific lines of code, suggest changes, or approve the pull request. The developer can then make any necessary updates and push them back to their forked repository, which will automatically update the pull request.
> Once all reviewers have approved the pull request and any conflicts have been resolved, it can be merged into the main branch of the original repository. This incorporates the proposed changes into the main codebase.
> Pull requests are an essential part of collaboration in git and GitHub as they provide a way for developers to contribute their changes while allowing for review and discussion before merging them into the main branch.

## Closing pull requests in Git

See also [[Closing pull requests in Git]]