Please summarize the following text. Use only the text itself as material for summarization, and do not add anything new. Rewrite this for brevity.

```js quickadd
const videoUrl = await this.quickAddApi.utility.getClipboard(); //await this.quickAddApi.inputPrompt("Video URL");

const url = new URL(videoUrl);
const videoId = url.searchParams.get('v');

this.variables["📺 YouTube Video ID"] = videoId;

const transcriptBody = await requestUrl(`https://youtubetranscript.com/?server_vid2=${videoId}`).text;
const videoPage = await requestUrl(videoUrl).text;

console.log(transcriptBody);
console.log(videoPage);

const dp = new DOMParser();
const dom = dp.parseFromString(transcriptBody, 'text/xml');
const transcriptEl = dom.getElementsByTagName('transcript')[0];
if (!transcriptEl) {
	new Notice("No transcript found.");
	throw new Error("No transcript found.")
}
const textElements = transcriptEl.getElementsByTagName('text');

const textArr = [];
for (let i = 0; i < textElements.length; i++) {
  const text = textElements[i];
  textArr.push(text.textContent);
}

const transcript = textArr.join("\n");

const title = videoPage.split('')[1].split('')[0].replace(" - YouTube", '').trim();

function sanitizeFileName(fileName) {
  const illegalChars = /[\/\?<>\\:\*\|"]/g;
  const undesiredChars = /"/g;
  const replacementChar = '_';
  return fileName.replace(illegalChars, replacementChar).replace(undesiredChars, "");
}

function sanetizeTitle(text) {
  const undesiredChars = /"/g;
  const replacementChar = "";
  return text.replace(undesiredChars, replacementChar);
}

this.variables["title"] = sanetizeTitle(title);
this.variables["safeTitle"] = sanitizeFileName(title);

return transcript;
```