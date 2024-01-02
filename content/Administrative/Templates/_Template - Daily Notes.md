---
daily-notes: true
file-created: <%tp.file.title%>
file-modified: <%tp.file.title%>
tags:
  - dailynotes
sleep: 
mood: 
meditation: 
exercise: 
location:
importance: 
note-type:
  - diary
AutoNoteMover: disable
---

# <% tp.date.now("dddd MMMM Do YYYY", 0, tp.file.title, "YYYY-MM-DD") %>
#dailynotes 
%% Daily Log %%
![[Happiness checklist to keep what is good and remove the bad#^happy-checklist]]

%% Monthly note link: [[<% tp.date.now("YYYY-MM", 0, tp.file.title, "YYYY-MM-DD") %>]]%%

---


## Daily events


## Watcha thinking about?



---
## Notes created today

```dataview

List FROM "" WHERE file-created = date("<%tp.file.title%>") SORT file.ctime desc

```

## Notes last modified today

```dataview

List FROM "" WHERE file-modified = date("<%tp.file.title%>") SORT file.mtime desc

```

