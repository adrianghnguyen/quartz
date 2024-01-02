
#admin/tips 



https://dannb.org/blog/2022/obsidian-daily-note-template/

Used the dataquery view from this website code in order to power how Obsidian checks for the notes created or edited today

It also uses the Templater plugin to populate the dates.

---

### Notes created today

```dataview

List FROM "" WHERE file.cday = date("<%tp.date.now("YYYY-MM-DD")%>") SORT file.ctime asc

```

### Notes last touched today

```dataview

List FROM "" WHERE file.mday = date("<%tp.date.now("YYYY-MM-DD")%>") SORT file.mtime asc

```