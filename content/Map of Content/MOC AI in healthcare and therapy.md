---
AutoNoteMover: disable
aliases: []
file-created: 2023-09-06
file-modified: 2023-09-06
moc: true
note-type:
  - map of content
---

#admin/moc 

# Content hub for MOC AI in healthcare and therapy

---



## All #society/healthcare AND #intelligence/artificial-intelligence AND #psychology/therapy

```dataview
	LIST
	FROM 
		(#society/healthcare AND #intelligence/artificial-intelligence) OR 
		(#intelligence/artificial-intelligence AND #psychology/therapy) 
		AND !#admin/moc AND !#people AND !#admin/private
	SORT file.name
```

## Searching all content with #society/healthcare OR #intelligence/artificial-intelligence OR #psychology/therapy
```dataview
	LIST
	FROM #society/healthcare OR #intelligence/artificial-intelligence OR #psychology/therapy AND !#admin/moc AND !#people AND !#admin/private
	SORT file.name
```

