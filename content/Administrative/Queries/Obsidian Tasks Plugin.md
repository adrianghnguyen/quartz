---
dg-publish: false
aliases:
  - Obsidian Tasks Plugin
tags:
  - admin/query
  - admin/obsidian-management
file-created: 2023-10-05
file-modified: 2023-10-05
note-type: 
description: 
linter-yaml-title-alias: Obsidian Tasks Plugin
---

# Obsidian Tasks Plugin

#status/wip

---

> [!Tip] [Quick Reference - Tasks User Guide - Obsidian Publish](https://publish.obsidian.md/tasks/Quick+Reference)
>
> [Tasks User Guide - Obsidian Publish](https://publish.obsidian.md/tasks/Queries/)
> [Filters - Tasks User Guide - Obsidian Publish](https://publish.obsidian.md/tasks/Queries/Filters)

- [Filters - Tasks User Guide - Obsidian Publish](https://publish.obsidian.md/tasks/Queries/Filters#Filters%20for%20File%20Properties)
	- Filter for specific file
	- Note that {{query.file.path}} is an alias placeholder

Search in current file
```tasks
path includes {{query.file.path}}
group by heading
```

Search by tag
```tasks
tags include #blahblah
```

Sorting keys:
- `sort by priority
- sort by urgency`