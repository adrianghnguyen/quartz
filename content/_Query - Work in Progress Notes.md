---
dg-permalink: 
aliases: _Query - Work in Progress Notes, wip notes,
tags: [admin/query]
file-created: 2022-11-13
file-modified: 2023-02-04
linter-yaml-title-alias: _Query - Work in Progress Notes
---

# _Query - Work in Progress Notes

Notes which have more links should be prioritized considering they are being related to more notes.

## Unpublished work in progress notes

```dataview
	TABLE 
		length(file.outlinks) + length(file.inlinks) AS "Links",
		dg-publish as "Published",
		date(today) - file-created AS "Since creation",
		date(today)- file-modified AS "Last modified",
		length(file.tags) AS "Tags" 
	FROM 
		#status/wip or ("Notes Central Hub/" AND !#status/done) or #status/postponed 
	WHERE 
		startswith(file.name,"_Template") = false
	SORT 
		dg-publish ASC,
		length(file.outlinks) + length(file.inlinks) DESC,
		file.cday DESC
	LIMIT 30
```


## WIP notes which have been published

```dataview
	TABLE 
		length(file.outlinks) + length(file.inlinks) AS "Links", 
		dg-publish as "Published",
		date(today) -file.cday AS "Since creation",
		date(today)-file-modified AS "Last modified",
		length(file.tags) AS "Tags" 
	FROM 
		#status/wip or ("Notes Central Hub/" AND !#status/done) or #status/postponed 
	WHERE 
		startswith(file.name,"_Template") = false and dg-publish = true
	SORT 
		dg-publish ASC,
		length(file.outlinks) + length(file.inlinks) DESC,
		file-created DESC
	LIMIT 30
```