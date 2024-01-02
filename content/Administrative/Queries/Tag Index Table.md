---
aliases:
file-created: 2023-02-07
dg-permalink: 
---

#admin/query   

---

```dataview
TABLE WITHOUT ID (tag + "(" + length(rows.file.link) + ")") AS Tags, (rows.file.link) AS Files
FROM ""
WHERE file.tags
FLATTEN file.tags AS tag
GROUP BY tag
SORT length(rows.file.link) DESC
```

