---
aliases: Reference Materials
tags: [reference-material]
file-created: 2023-03-20
file-modified: 2023-03-20
AutoNoteMover: disable
linter-yaml-title-alias: Reference Materials
---

#admin/moc

# Reference Materials

---

> [!info] Content scope
> All the content which I am reference and are not exactly original thoughts. You can consider them my literary notes. 

## Searching All Content with #reference-material 

```dataview
	TABLE 
	file-created as "Added",
	original-title as "Article Title",
	author as "Author",
	doc-type as "Type", 
	source as "Source"
	FROM #reference-material AND !#admin/moc AND !#people AND !#admin/private AND #status/done 
	WHERE dg-publish
	SORT file-created DESC
```
