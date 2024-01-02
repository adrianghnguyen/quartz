---
aliases: Closing pull requests in Git, pull requests, merging in git
file-created: 2023-07-06
file-modified: 2023-07-06
tags: computer-science/software-engineering
linter-yaml-title-alias: Closing pull requests in Git
dg-publish: true
---

# Closing pull requests in Git

#status/done

Related to [[Github]]

- [git - What is the difference between merge --squash and rebase? - Stack Overflow](https://stackoverflow.com/questions/2427238/what-is-the-difference-between-merge-squash-and-rebase)
- [How to Close a Pull Request - Merge Commit vs Squash vs Rebase on GitHub — Leonardo Montini](https://leonardomontini.dev/close-pr-strategy-merge-commit-squash-rebase/#:~:text=Merge%20commit%20has%20all%20tangled,extra%20commit%20for%20the%20merge.)

## The are three main types of ways to merge commits in Git

There are three main types of merging pull requests in Git which are ways of bringing commits onto another branch.

Guidelines:
- Use Git Merge Commit when preserving a detailed history is important
- Use Squash Merge to simplify the commit history
- Use Rebase to incorporate latest changes while maintaining a cleaner, linear history

## Git Merge Commit

  - Regular merge creates a merge commit with multiple parent commits
  - Preserves entire history of both branches
  - Useful for maintaining a detailed history and visibility of changes made

## Squash Merge

  - Combines multiple commits into a single, coherent commit
  - Condenses changes from branch being merged
  - Results in a cleaner, more concise history

### Workaround for the digital garden

In the case of [[Notes Central Hub/My Projects/Publishing my digital garden|my digital garden]], this is probably the best way of bringing in a lot of my commits since I write a lot on the main branch. Every commit would trigger a build job which would trigger the API request limit on Vercel. As a workaround, I created a deployment branch where I do manual pull requests and do a squash merge to only trigger the occasional build.

## Rebase

  - Moves or combines a sequence of commits to a new base commit
  - Changes the base of a branch
  - Helps in incorporating latest changes from another branch
  - Results in a linear commit history
