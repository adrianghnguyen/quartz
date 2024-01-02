---
aliases:
  - Visual Studio Code
  - VS Code Editor
  - code editor
tags:
  - computer-science/programming
file-created: 2023-04-17
file-modified: 2023-09-02
note-type: general
description: 
linter-yaml-title-alias: Visual Studio Code
---

# Visual Studio Code

#status/postponed

---

## What is visual studio code?

> [!ai]+ AI
>
> Visual Studio Code (VS Code) is a free, open-source code editor developed by Microsoft. It is designed to be lightweight and fast while also offering powerful features for editing and debugging code. VS Code is compatible with multiple [[Programming languages]], including Java, Python, JavaScript, and many others. It also includes extensions that allow developers to customize their workspace and add features specific to their needs. VS Code is available on Windows, Mac, and Linux operating systems. It has become a popular choice among developers due to its ease of use and versatility for various programming environments.

I'm currently using as my primary code editor. It's lightweight and resembles [[Why I write in Obsidian|Obsidian]] in a lot of ways.

## Allowing execution rights within VS Code

This error occurs because PowerShell script execution is disabled on your system, and VS Code is trying to execute an npm command that requires script execution. To fix this error within VS Code, you can enable script execution for PowerShell within the integrated terminal. Here's how:

1.  Open the integrated terminal in VS Code by pressing Ctrl + ` (backtick).
2.  Check the current execution policy by running the following command in the terminal:

	`Get-ExecutionPolicy`

	This will return the current execution policy. If it's set to "Restricted", you won't be able to run scripts.

3.  To enable script execution for the current user, run the following command in the terminal:

	`Set-ExecutionPolicy -Scope CurrentUser RemoteSigned`

	This will allow scripts signed by a trusted publisher to run for the current user.

4.  You'll be prompted to confirm the change. Type "Y" and press Enter.
5.  Try running your npm command again in the terminal.
