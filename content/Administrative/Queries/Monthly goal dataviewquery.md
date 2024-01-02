---
dg-publish: 
aliases:
  - Monthly goal query
tags:
  - admin/query
  - admin
file-created: 2023-09-05
file-modified: 2023-09-25
note-type:
  - queries
description: 
linter-yaml-title-alias: Monthly goal query
review: 
---

# Monthly goal query

---

## Older than a month

```dataview return last month goals
TASK 
FROM #dailynotes/monthly 
WHERE date(today) - dur(1 mo) > date(monthly-date)
```

^8f94a3

## All monthly goals
```dataview return last month goals
TASK 
FROM #dailynotes/monthly 
```

## Current monthly goals

```dataview return last month goals
TASK 
FROM #dailynotes/monthly 
WHERE date(today) - dur(1 mo) < date(monthly-date)
```