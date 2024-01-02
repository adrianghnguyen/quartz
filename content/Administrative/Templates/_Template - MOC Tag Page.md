---
AutoNoteMover: disable
aliases: []
file-created: <%tp.file.creation_date("YYYY-MM-DD")%>
file-modified: <%tp.file.creation_date("YYYY-MM-DD")%>
moc: true
note-type:
  - map of content
---

#admin/moc 

# Content hub for <% tp.file.title %>

---

<%*
  let title = tp.file.title
  if (title.startsWith("MOC untitled")) {
	title = await tp.system.prompt("Name of MOC");
	await tp.file.rename("MOC "+`${title}`);
  }
  tR
%>
