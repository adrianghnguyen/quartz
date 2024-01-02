---
dg-publish: true
aliases: Context on my vercel publishing issue, blog publishing issues
file-created: 2023-03-13
file-modified: 2023-05-05
tags: [personal/tech]
linter-yaml-title-alias: Context on my vercel publishing issue
---

# Context on my vercel publishing issue

#status/done

Related to [[Continuous Integration and Deployment]]

---

- So I've been using Vercel as my serverless web app deployment for my Obsidian second brain via the digital garden plugin.
- Recently, I've come into the problem that some links are broken…which I suspected happened during some kind of deployment but I can't identify which…oops we've gone too far
- I can take this as a learning opportunity to see how I can learn from best software engineering practices in terms of implementing a good CI pipeline…like not pushing to production automatically
[dead links urls not in same format as live links · Issue #66 · oleeskild/obsidian-digital-garden · GitHub](https://github.com/oleeskild/obsidian-digital-garden/issues/66) ???

https://adrian-public-digital-garden-git-dependab-9eaff6-adrianghnguyen.vercel.app/notes-central-hub/books/bearing-the-unbearable-by-joanne-cacciatore/

Revert to this template? [Pull 7](https://github.com/adrianghnguyen/adrian-public-digital-garden/pull/7)

## Who can help me?

- [[Tim Trinh|Papa]] <- knows a lot about good software architecture. I'll get roasted haha
- [[Tim Vieregge]] <- Probably worked with similar issues?

## Diagnosing the issue

### Weird settings message?

![[Pasted image 20230301082946.png]]

[Settings - Vercel](https://vercel.com/adrianghnguyen/adrian-public-digital-garden/settings/general) In my settings page, I have this message. I'm not sure when this configuration override was introduced or if it's beneficial but I've noticed that in a lot of my broken links, it's because the URL was not substituted appropriately

### Many notes need to be redeployed and broken links

![[Pasted image 20230301083151.png]]

For example, data engineering was previously published but trying to follow it there, for some reason it doesn't register as having been deployed?

### Dead homepage

I fixed this with a rollback but at some point, I had a blank page as my homepage.

### Bad url generation?

https://adrian-public-digital-garden.vercel.app/notes/apologizing-sincerely/ vs when linked from a map of content it gives this URL

https://adrian-public-digital-garden.vercel.app/notes/notes-central-hub-hobbies-bicycle-maintenance

^ Notice how it puts in the note-central-hub into the url which messes it up

### Stuck on cache build for sidebar?

Like the sidebar tree doesn't seem to be updating properly

## Possible fixes and next steps

Need to reflect upon this once we've diagnosed the issue well

1. Nuke the deployment environment and rebuild from scratch
2. Selectively rebuild? I don't know what command I need to do.
	1. Look into the next.js package? `npm build` command?
	2. [Configuring a Build | Vercel Docs](https://vercel.com/docs/concepts/deployments/configure-a-build)
3. Implement some best practices in terms of sending to a preview branch then graduating it to the production environment
	1. Downside is that means I won't be publishing as often - but CI pipeline checks could help make that faster/automate that for me
	2. Intermediary step is maybe not publishing as often and manually reviewing

4634

upload text giving bad URL?

```js
uploadToGithub(path, content) {
    return __async(this, null, function* () {
      if (!this.settings.githubRepo) {
        new import_obsidian2.Notice("Config error: You need to define a GitHub repo in the plugin settings");
        throw {};
      }
      if (!this.settings.githubUserName) {
        new import_obsidian2.Notice("Config error: You need to define a GitHub Username in the plugin settings");
        throw {};
      }
      if (!this.settings.githubToken) {
        new import_obsidian2.Notice("Config error: You need to define a GitHub Token in the plugin settings");
        throw {};
      }
      const octokit = new Octokit({ auth: this.settings.githubToken });
      const payload = {
        owner: this.settings.githubUserName,
        repo: this.settings.githubRepo,
        path,
        message: `Add content ${path}`,
        content,
        sha: ""
      };
      try {
        const response = yield octokit.request("GET /repos/{owner}/{repo}/contents/{path}", {
          owner: this.settings.githubUserName,
          repo: this.settings.githubRepo,
          path
        });
        if (response.status === 200 && response.data.type === "file") {
          payload.sha = response.data.sha;
        }
      } catch (e) {
        console.log(e);
      }
      payload.message = `Update content ${path}`;
      yield octokit.request("PUT /repos/{owner}/{repo}/contents/{path}", payload);
    });
  }
  uploadText(filePath, content) {
    return __async(this, null, function* () {
      content = gBase64.encode(content);
      const path = `src/site/notes/${filePath}`;
      yield this.uploadToGithub(path, content);
    });
```

## Solution

So turns out it was more simple than I thought. It was because sometimes the build would not render out some pages in the /src/ folder. As a result, the links became broken. I also think one of the dependency updates broke how permalinks were generated.

```c
uploadText(filePath, content) {
    return __async(this, null, function* () {
      content = gBase64.encode(content);
      const path = `src/site/notes/${filePath}`;
```

From what I understand about the pipeline, it assigns a permalink based on the file path.


## Ignoring build steps

[How to ignore Vercel build step for certain folders and files • Alfonso's Website](https://www.alfonsobries.com/posts/how-to-ignore-vercel-build-step-for-certain-folders-and-files)