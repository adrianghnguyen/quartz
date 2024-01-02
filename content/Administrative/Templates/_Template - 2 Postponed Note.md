---
dg-publish: 
topic: 
note-type:
  - general
review:
---

<%*
  let title = tp.file.title
  if (title.startsWith("Untitled")) {
    title = await tp.system.prompt("Title");
    await tp.file.rename(`${title}`);
  } 
  tR
%>

#status/postponed  

---

