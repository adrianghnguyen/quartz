---
aliases:
  - Renaming file titles dynamically
tags:
  - 
file-created: 2023-02-27
file-modified: 2023-09-03
note-type: 
description: 
linter-yaml-title-alias: Renaming file titles dynamically
---

# Renaming file titles dynamically

#status/wip

Executes a text prompt then renames the file accordingly
```
<%*
  let title = tp.file.title
  if (title.startsWith("Untitled")) {
    title = await tp.system.prompt("Title");
    await tp.file.rename(`${title}`);
  } 
  tR
%>
---
# <%* tR += `${title}` %>
```
