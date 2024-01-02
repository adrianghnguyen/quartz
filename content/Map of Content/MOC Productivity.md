---
AutoNoteMover:
  - disable
aliases:
  - Content hub for Productivity
file-created: 2023-09-05
file-modified: 2023-09-05
moc: true
note-type:
  - map of content
dg-publish: true
---

#admin/moc 

# Content hub for Productivity

---

## Searching all content with #productivity
```dataview
	LIST
	FROM #productivity AND !#admin/moc AND !#people AND !#admin/private
	SORT file.name
```