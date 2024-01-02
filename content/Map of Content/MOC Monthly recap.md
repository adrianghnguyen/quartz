---
AutoNoteMover: disable
aliases: MOC Monthly recap, all monthly reviews
file-created: 2023-08-22
file-modified: 2023-08-22
---

#admin/moc 

# MOC Monthly recap

---

> [!info] Content scope
> My bubbled up monthly reviews where I do more long-term planning and think about what things happened.

## Monthly task tracker
```tasks
tags include #dailynotes/monthly 
```


## Searching all content with #dailynotes/monthly
```dataview
	table 
		linter-yaml-title-alias
	FROM #dailynotes/monthly AND !#admin/moc AND !#people AND !#admin/private 
	WHERE !contains(file.path, "Templates")
	SORT file.name
```
