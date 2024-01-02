---
start: <% tp.date.now("YYYY-MM-DD") %>
introduction: 
description: 
birthday: 
relationship: []
location: []
company: 
contact: 
likes: []
dislikes: []
goals: 
occupation: 
skills: 
note-type:
  - contact
tags:
  - people
  - admin/private
aliases:
---


## Notes
%% Key dates, anything in particular %%

---
## Referenced in notes

```dataview
table 
	date(today) - date(file.name) AS "Since" 
from [[]] AND !#folder
SORT daily-notes DESC, file-created DESC
```