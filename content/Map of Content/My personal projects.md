---
note-type: 
aliases:
  - My Projects
  - project dashboard
  - my personal projects
  - personal projects MOC
  - things I want to work on
  - recent projects
linter-yaml-title-alias: My Projects
tags:
  - admin/moc
  - my-projects
dg-publish: false
dg-permalink: "202303031645"
file-created: 2023-01-21
file-modified: 2023-03-16
---

# My Projects

> [!NOTE] Content scope
> Covers all my personal projects and displays their overall status,
>
> - [[My personal project management process]]
> - [[Deliberate practice leads to mastery]] is why I pursue projects

[[Interesting Project Ideas|Interesting personal projects and ideas]]
## Projects Dashboard Query

```dataview
	TABLE 
	description AS "One-liner Summary",
	start AS "Started",
	end AS "Finished", 
	progress As Status
	FROM #my-projects AND !#admin/moc
	WHERE !contains(file.path, "Templates")
	SORT progress, start DESC, file-created DESC
```
