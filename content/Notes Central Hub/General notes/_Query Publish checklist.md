---
aliases:
  - Query Publish checklist
  - Digital garden publishing checklist
file-created: 2023-02-27
file-modified: 2023-09-01
tags:
  - admin/query
linter-yaml-title-alias: Query Publish checklist
---

# Query Publish checklist

---

Also see [[_Query - Work in Progress Notes]]

## Done and not published -> Add publish flag

```dataview
	TABLE file.path, dg-publish
	FROM #status/done AND !#admin/private AND !"Administrative" AND !#reference-material 
	WHERE dg-publish = null
```

## Postponed and published -> Switch to status/done

```dataview
	TABLE file.path, dg-publish
	FROM #status/postponed  AND !#admin/private AND !"Administrative" AND "POSTPONED - Writing"
	WHERE dg-publish = true
```

## Published but in wrong location? -> Unpublish or change status tag

```dataview
	TABLE file.path, dg-publish
	FROM !"Notes Central Hub" AND !"Reference Materials" AND !"Map of Content" AND !"Administrative/Templates"
	WHERE dg-publish = true
```
