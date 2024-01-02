---
dg-publish: true
aliases:
  - Book Queries
  - queries for books
  - dataview queries for books
tags:
  - book
  - admin/query
file-created: 2023-03-13
file-modified: 2023-09-21
note-type:
  - queries
description: 
linter-yaml-title-alias: Book Queries
---

# Book Queries

#status/done

---
%%

## About This Page

> [!warning] This ain't it chief
> This page is to hold all my book related queries together so it's easier to just manage them from one central place. It's not meant to do content writing

- See [[01 List of all books]]

### Metadata Book Attributes

%%

## List of All Books

%%Basic query block for books%%

```dataview
TABLE WITHOUT ID
	progress as "Progress",
	category as "Category",
	"![|60](" + cover + ")" as Cover,
	link(file.link, title) as Title,
	author as Author,
	start as "Start",
	end as "Done"
FROM #Book AND !#admin/moc and !#admin
WHERE !contains(file.path, "Templates")
SORT progress desc, file.ctime DESC 
```

## Currently reading

```dataview
TABLE WITHOUT ID
	f_progress as "Progress",
	category as "Category",
	"![|60](" + cover + ")" as Cover,
	link(file.link, title) as Title,
	author as Author,
	start as "Start",
	end as "Done"
FROM #Book AND !#admin/moc and !#admin
FLATTEN progress as f_progress
WHERE f_progress = "in-progress"
SORT progress desc, file.ctime DESC 
```

## Completed Books

%% reading-status = "done" %%

```dataview
TABLE WITHOUT ID
	f_progress as "Progress",
	category as "Category",
	"![|60](" + cover + ")" as Cover,
	link(file.link, title) as Title,
	author as Author,
	start as "Start",
	end as "Done"
FROM #Book AND !#admin/moc and !#admin
FLATTEN progress as f_progress
WHERE f_progress = "done"
SORT progress desc, file.ctime DESC 
```

## Unread Books

```dataview
TABLE WITHOUT ID
	f_progress as "Progress",
	category as "Category",
	"![|60](" + cover + ")" as Cover,
	link(file.link, title) as Title,
	author as Author,
	start as "Start",
	end as "Done"
FROM #Book AND !#admin/moc and !#admin
FLATTEN progress as f_progress
WHERE f_progress = "upcoming" AND !contains(file.path, "Templates")
SORT progress desc, file.ctime DESC 
```