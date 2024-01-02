---
note-type:
  - general
  - diary
review:
---

#admin/private/personal 

---

<%*
  let title = tp.file.title
  if (title.startsWith("Untitled")) {
	title = tp.file.creation_date("YYYY-MM-DD HHmm");
	await tp.file.rename(`${title}`);
  }
  tR
%>


<% tp.file.cursor(1)%>