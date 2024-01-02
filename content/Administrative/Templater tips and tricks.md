---
aliases:
  - Templater Tips and Tricks
  - tips for Obsidian Plugin templater
file-created: 2023-03-13
file-modified: 2023-08-30
tags:
  - admin
  - admin/obsidian-management
linter-yaml-title-alias: Templater Tips and Tricks
---

# Templater Tips and Tricks

This renders out the current date in a specific format (first parenthesis) for templater

```
<% tp.date.now("dddd Do MMMM, YYYY", 0, tp.file.title, "YYYY-MM-DD")%>
```

## How to interact with system related functions such as the clipboard or a prompt or suggester

[tp.system - Templater](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/system-module.html)

```
Clipboard content: <% tp.system.clipboard() %>

Entered value: <% tp.system.prompt("Please enter a value") %>
Mood today: <% tp.system.prompt("What is your mood today ?", "happy") %>

Mood today: <% tp.system.suggester(["Happy", "Sad", "Confused"], ["Happy", "Sad", "Confused"]) %>
Picked file: [[<% (await tp.system.suggester((item) => item.basename, app.vault.getMarkdownFiles())).basename %>]]
```

`<% tp.system.prompt("Sleep quality rating? (1-10)") %>`

## Rename untitled files on creations if matching name to untitled

```
<%*
  let title = tp.file.title
  if (title.startsWith("Untitled")) {
	title = await tp.system.prompt("Title");
	await tp.file.rename(`${title}`);
  }
  tR
%>
```

## Place file cursor

Set file cursor locaiton, can change the number to make it go through multiple places
```
<% tp.file.cursor(1) %>
```

## [How to output a value from a JavaScript Execution Command ?](https://silentvoid13.github.io/Templater/commands/execution-command.html?highlight=engine%20scoped#how-to-output-a-value-from-a-javascript-execution-command-)

> Sometimes, you may want to output something when using a JS execution command.
> 
> When our templating ==engine== generates a replacement string using all of our commands results, it is stored in a variable named `tR`. This is the string that will contain the processed file content. You are allowed to access that variable from a JS execution command.
> 
> This means that, to output something from a JS execution command, you just need to append what you want to output to that `tR` string variable.
> 
> For example, the following command: `<%* tR += "test" %>` will output `test`.


```
<%* if (tp.file.title.startsWith("Hello")) { %>
This is a hello file !
<%* } else { %>
This is a normal file !
<%* } %>
    
<%* if (tp.frontmatter.type === "seedling") { %>
This is a seedling file !
<%* } else { %>
This is a normal file !
<%* } %>
    
<%* if (tp.file.tags.contains("#todo")) { %>
This is a todo file !
<%* } else { %>
This is a finished file !
<%* } %>

<%*
function log(msg) {
    console.log(msg);
}
%>
<%* log("Title: " + tp.file.title) %>
    
<%* tR += tp.file.content.replace(/stuff/, "things"); %>

```

