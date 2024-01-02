---
dg-publish: true
aliases: MOC Personal evaluations, personal evaluations
file-created: 2023-07-18
file-modified: 2023-07-27
tags: [measurement/survey]
AutoNoteMover: disable
linter-yaml-title-alias: MOC Personal evaluations
---

#admin/moc

# MOC Personal evaluations

---

> [!info] Content scope
> Psychological surveys or things which provide personal evaluations

> [!todo] Fix exercise: true regex to personal-evaluation: true

## Searching personal evaluations

```dataview
	LIST
	FROM !#people AND !#admin/private
	WHERE personal-evaluation
	SORT file.name
```
