---
dg-publish: true
aliases: Recently Published Files, recently modified
file-created: 2023-01-30
file-modified: 2023-06-21
tags: [admin/query]
linter-yaml-title-alias: Recently Published Files
source: 
---

#status/done #admin/moc

# _01 Recently Published Files

Files which have been recently created and have been published. %%See also [[_Query Publish checklist|unpublished articles]]%%

## Recently published files based on creation date

```dataview
	TABLE file-created as "Created", file.mday as "Modified"
	FROM !"Administrative" AND !#admin AND !#admin/moc AND !#book AND !#kindle-highlights and !#reference-material
	WHERE file-created AND dg-publish
	SORT file-created DESC
	LIMIT 30
```

## Recently edited files

```dataview
	TABLE 
		file-modified as "Edited",
		date(today) - file-modified as "Since"
	FROM 
		!"Administrative" AND !#admin AND !#admin/moc AND !#book AND !#kindle-highlights AND !#reference-material
	WHERE file-created AND dg-publish
	SORT file-modified DESC
	LIMIT 50
```
