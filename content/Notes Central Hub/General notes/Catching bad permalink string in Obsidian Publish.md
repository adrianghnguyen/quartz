---
dg-publish: true
aliases: Catching bad permalink string in obsidian publish, publishing notes
file-created: 2023-02-11
file-modified: 2023-05-05
tags: [admin/obsidian-management, computer-science/programming, computer-science/programming]
linter-yaml-title-alias: Catching bad permalink string in obsidian publish
---

# Catching bad permalink string in obsidian publish

#status/done

---

## Process to fix bad permalinks

1. Try to publish multiple notes within Obsidian then it throws error
2. Open up Notepad++ and open up Obsidian directory
3. Right click on Notes Central Hub folder and click on "Find in files…"
4. In find search bar, I can put in regex expression
	1. The one to catch permalinks that have permalink url without surrounding quotes is the following
		1. `dg-permalink: [\d?]`
5. Go and edit those files then save them

### Found regex solution string

`dg-permalink: [\d?]`

### Look for these watch variables within [[Debugging ElectronJS]]

![[Pasted image 20230216152439.png]]

## Use case

I want to catch `dg-permalink: 3290347978` <-there's no quotes to turn the number into a string
