---
aliases:
  - Publishing Obsidian notes
tags:
  - admin/obsidian-management
  - productivity
file-created: 2023-02-27
file-modified: 2023-09-03
note-type: 
description: 
linter-yaml-title-alias: Publishing Obsidian notes
---

# Publishing Obsidian notes

- Ended up using this: https://dg-docs.ole.dev/getting-started/01-getting-started/
- Uses netlify and Vercel to do a CI pipeline which builds a static webpage from github using the Digital Gardens Obsidian plugin
- To set notes to be published, you need to add the following value into the frontmatter
	- `dg-publish: true`
	- To mass-edit this value, I installed the MetaEdit plugin. Right-clicking the [[Notes Central Hub]] folder allows me to add the property `dg-publish` and set the value to `true`
		- ![[Pasted image 20230124212910.png]]
- Afterwards, use the command palette to execute the command `Digital Garden: Publish notes`
Website lives here: https://adrian-public-digital-garden.vercel.app/
- API token set to expire every 90 days

---

## Other references - unused

Check the other one as well
https://quartz.jzhao.xyz/
- Github workflow to deploy to github pages directly
- Making some notes private by not publishing - https://discourse.gohugo.io/t/ignore-a-directory/8880
- How to publish Obsidian notes for free
https://about.gitlab.com/blog/2022/03/15/publishing-obsidian-notes-with-gitlab-pages/

### How to Publish Your Obsidian Notes Online For Free
