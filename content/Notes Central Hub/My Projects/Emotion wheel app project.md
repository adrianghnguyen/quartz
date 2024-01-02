---
aliases:
  - Emotion wheel app
  - emotion web app
  - emotional feelings wheel app project
  - emotion decoding project
  - emotion dictionary app
  - emotional compass project
tags:
  - my-projects
note-type:
  - project
description: 
progress:
  - backlog
  - in-progress
file-created: 2023-11-06
file-modified: 2023-12-30
start: 2023-11-06
end: 
difficulty:
  - medium
linter-yaml-title-alias: Emotion wheel app
published: true
---

# Emotion wheel app

- Create an emotion wheel app
- People can write in how they're feeling, it tells them what they are most likely feeling
- Hover over an emotion and have it described
	- [Feelings Wheel](https://feelingswheel.com/)

## Goals and Key success factors %% fold %%

- Program side
	- User can input text
	- User receives results of detected emotion
	- User receives feedback on what emotion was detected
- Understand how LLM was trained to classify emotion task
- Understand what resulting scores represent
- The objective is to learn how to deploy python to a web environment using Flask

### Desired functionalities, behaviours and expectations %% fold %%

Things I want the project to have by the end
- UI side
	- Display input box + submit button
	- Explain the purpose of this project/provide context
	- Looks like a modern or non ugly looking page design (use Bootstrap?)
	- Display emotion detected scores
	- Display label definition
	- After results, have a button to go back to home/redirect to home
- Functionalities
	- Allow user to retrigger or reprocess the emotions according to a new threshold. Alternatively, is there a way to dynamically only show elements if they have a certain user-value without needing to reload the page or re-trigger.
	- Allow user to enter in text and retrieve a page response
	- Intake text through emotion labeling model to determine scores
	- Hosted on an external server/not local host
	- Ability to split multi-line text?

## Project resources and notes %% fold %%

> [!Info]
>  Brainstorming dump: [[Emotion wheel app project.canvas|Emotion wheel app project canvas]]

- [The Feelings Wheel: unlock the power of your emotions — Calm Blog](https://www.calm.com/blog/the-feelings-wheel)
- [Feelings Wheel](https://feelingswheel.com/)
- [[Google Colab]]
- [[Javascript|Javascript]]

### Technical project notes

#### WebStorage API

- Can store session data and maintain browser data. Might want to look into `localStorage` which can persist after browser is closed/reopened
- [ChatGPT](https://chat.openai.com/share/ff2d1550-fbb5-42d5-9576-b6efe1f1f53f)
- [How the Web Storage API Works](https://www.telerik.com/blogs/how-web-storage-api-works)
- [Web Storage API - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API)

##### Exporting ansd importing data with localstorage


[Chrome Extension: Local Storage, how to export - Stack Overflow](https://stackoverflow.com/questions/23160600/chrome-extension-local-storage-how-to-export)
```javascript
chrome.storage.local.get(null, function(items) { // null implies all items
	// Convert object to a string.
	var result = JSON.stringify(items);

	// Save as file
	var url = 'data:application/json;base64,' + btoa(result);
	chrome.downloads.download({
		url: url,
		filename: 'filename_of_exported_file.json'
	});
});
```

[javascript - Using Google Chrome extensions to import/export JSON files? - Stack Overflow](https://stackoverflow.com/questions/38833178/using-google-chrome-extensions-to-import-export-json-files/38838572#38838572)

#### The machine learning model for encoding emotions

- [GoEmotions: A Dataset of Fine-Grained Emotions | Papers With Code](https://paperswithcode.com/paper/goemotions-a-dataset-of-fine-grained-emotions) - paper which describes the dataset which uses it
- Some researchers built something quite similar to what I did in this paper: [Frontiers | Detection of emotion by text analysis using machine learning](https://www.frontiersin.org/articles/10.3389/fpsyg.2023.1190326/full) where they created a website which allows users to input text, and detect emotions accordingly.

#### Learning Flask and web deployments

- [[Flask web app framework]]
- [[REF Free-For-Dev development resources|REF GitHub - ripienaar/free-for-dev: A list of SaaS, PaaS and IaaS offerings that have free tiers of interest to devops and infradev]]

#### Deploying an app to production

- [My Journey to a serverless transformers pipeline on Google Cloud](https://huggingface.co/blog/how-to-deploy-a-pipeline-to-google-clouds) May be useful? They use Google App Engine

### How should people understand how to use this app?

Learn more about the concept of a feelings wheel

> The Feelings Wheel offers a unique and nuanced approach to identifying and comprehending emotions. It’s a tool that allows individuals to better navigate their inner emotional landscapes and foster healthier emotional intelligence.
>
> The Feelings Wheel can serve as a guide to understand the intricate web of emotions we all feel and their interconnectedness with other emotions. It’s a powerful tool that can help you explore your feelings more deeply and also express them more accurately so you can get the support you need, or simply process whatever emotions you’re navigating.
>
> Benefits:
> - Help you communicate more effectively by understand in more details what you may be feeling
> - Provides mindful reflection and enhances emotional awareness
> - Supports emotional regulation through the ability to identify and label your emotions your feelings
>

[[Designing the user experience of the Emotional compass]]

## Project diary and tasks %% fold %%

```tasks
path includes {{query.file.path}}
sort by priority
group by status.name
short mode
```

### Task entries

%% General dump of things I need to do %%
- [-] Research list of JSON objects and how to manipulate them ➕ 2023-12-29
- [ ] Add analytics summary page (reads through entire entry array) ➕ 2023-12-29
- [x] Deploy to Heroku to gather feedback ⏫ ➕ 2023-12-29 ✅ 2023-12-29
- [x] Write content information on what a feelings wheel is/how to use? Maybe ask friends for feedback on how they'd write it. ➕ 2023-12-29 ✅ 2023-12-31
- [x] Rename to 'Emotion compass' ➕ 2023-12-30 ✅ 2023-12-30
- [x] Write down what is an emotional compass blurb/website ➕ 2023-12-30 ✅ 2023-12-31
- [x] Rename input to "Write about your day or a situation…" ➕ 2023-12-30 ✅ 2023-12-30
- [x] Create a Feedback section ➕ 2023-12-30 ✅ 2023-12-30
	- Add a callout saying 'I need help with…'
	- Planned features / Under consideration
- [x] Implement a hardcoded character limit (how hard is it do a word count element?) ➕ 2023-12-30 ✅ 2023-12-31
- [>] Think about emotion synonym features for each scored label 🔽 ➕ 2023-12-30
- [>] Display a colored box around the emotion label to represent to which cluster it belongs (positive/negative/amb/neutral) ⏬ ➕ 2023-12-30
- [>] Popover to provide definition description? 🔽 ➕ 2023-12-30
- [ ] Explain how the data is stored ➕ 2023-12-30
- [ ] Fix spacing on the submit button 🔽 ➕ 2023-12-30
- [ ] Implement export data feature ⏫ ➕ 2023-12-31
- [ ] Research on 3 journaling apps ➕ 2023-12-31
### Daily entries %% fold %%

- [[2023-11-06]] %% fold %%
	- Start by talking, decode emotions
	- Can add functionality of detecting emotions based on the voice
	- Display which emotions are most likely detected
		- Display spider chart?
		- Display the transcribed text and highlight which particular words indicated what…under the hood? Is that even possible? Most LLMs only spit an output and are more of a black box.
		- Feeling wheel
	- Tell me how you're feeling
		- User input
		- Process
		- Spit results
	- Take the feelings wheel and allow people to hover over to see a tooltip of emotion
		- [https://feelingswheel.com/](https://feelingswheel.com/)
		- Hey it seems like you're feeling…
		- Link to resources / display definition of the appropriate emotion
- [[2023-11-29]] %% fold %%
	- It's been a while since I work on this - what do I have? What do I still need to build? What needs to work in the first version of this?
		- The dataset powering the model is the following: [GoEmotions: A Dataset of Fine-Grained Emotions | Papers With Code](https://paperswithcode.com/paper/goemotions-a-dataset-of-fine-grained-emotions) where I can learn more about the dataset itself
			- [[REF GoEmotions A Dataset of Fine-Grained Emotions|GoEmotions dataset]] taken here
- [[2023-11-30]] %% fold %%
	- Consider swapping this out for this model which is faster for small batches - something to think about for the future
		- [SamLowe/roberta-base-go\_emotions-onnx · Hugging Face](https://huggingface.co/SamLowe/roberta-base-go_emotions-onnx)
		- There are already areas for which I think I can optimize, but maybe that's for later. Let's get it working then we can worry about it after we have a better idea of the structure.
- [[2023-12-13]] %% fold %%
	- Rebuilt from scratch. Got a nice few nice loop comprehensions working. [[My personal accomplishments and victories|Nice.]] The important part is just to [[Building momentum and getting things started|get the ball rolling]].
		- For future task but consider swapping it into a class/object to make it easier to maintain
- [[2023-12-14]] %% fold %%
	- Got it working into a class
	- Now trying to understand how to place it into Flask
	- [x] Create hello world using Flask ✅ 2023-12-14
	- [x] display static text using Flask ✅ 2023-12-14
	- [x] Using hard-coded input redirect printed text from my class to page ✅ 2023-12-15
	- [x] Find out how to receive input text as variable from web page ✅ 2023-12-15
	- [x] Pass input text variable into class ✅ 2023-12-15
	- [x] Tie it all together to print it out ✅ 2023-12-18
- [[2023-12-15]] %% fold %%
	- Tied the decoding emotion logic into the flask backend. Nice!
	- How do engineers ensure API standards consistency when changing back end logic? Do they us something like design patterns?
- [[2023-12-16]] %% fold %%
	- Once I have the initial skeleton function working, what else do I want to add?
	- Can I use bootstrap to not make everything fugly?
		- Is it something I can just add into the HTML and then the browser handles the Javascript?
		- Okay for now, let's get the raw HTML into somewhere decent and we can decide afterwards how to incorporate Bootstrap.
	- How do I send something like this post [My fiance (M33) thinks my (F36) job is meaningless and doesn't contribute to society. Should I still stay with him? : r/relationships](https://www.reddit.com/r/relationships/comments/18jwf72/my_fiance_m33_thinks_my_f36_job_is_meaningless/) into a post request?
		- Getting carriage return and LF characters.
	- Looks like I need to modify it to send the json object of a post request to the resource rather than it being directly in the URL?
		- [Python Requests post Method](https://www.w3schools.com/python/ref_requests_post.asp)
- [[2023-12-17]] %% fold %%
	- Talked with [[Tim Vieregge]] and he suggested I should avoid using a class-based strategy and mutate data (?) and instead make functions which return data.
	- There's a concept of 'don't build what you don't need' which states to not overplan for the future
	- I should use the `requests` package to send data payloads through. There are some tutorial videos to look at.
- [[2023-12-18]] %% fold %%
	- [[Tim Vieregge|Tim]] mentioned that what I'm trying to do is sending form data
	- [Sending form data - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data)
	- [Flask: Web Forms — Python Beginners documentation](https://python-adv-web-apps.readthedocs.io/en/latest/flask_forms.html)
	- Okay cool - got it working and the form works well.
	- Captured some notes in [[Website development|Website development]]
	- Trying to find out how to render
- [[2023-12-19]] %% fold %%
	- Getting feedback from [[Poe Han Thar Kyaw|Poe Han Thar Kyaw]] on the proof of concept version
		- [x] Have a customized version of the feelings wheel picture and have the scores overlaid on it ✅ 2023-12-27
			- Represent proportion of emotions based on scores
			- Customized animation `d3.js`
		- [x] Being able to write a whole day and being able to look back (timeline/per session) ✅ 2023-12-27
			- Ways to implement local data storage?
			- Export session?
			- Implement session login?
			- Implement cookies?
		- [x] Implement a definition of neutral ✅ 2023-12-27
- [[2023-12-22]]
	- Get google colab working…but no go.
	- Implement d3.js animation
	- [x] Implement local browser data cache using `webstorage` ✅ 2023-12-23
- [[2023-12-23]]
	- I spent 3 hours trying to fix why it wasn't parsing the json object properly. I needed to specify in the jinja template `{{ variable | tojson }}` otherwise it gets autoescaped as a string. FML.
	- Got the console printout working. Had to trace and really think about how my data was structured then get accustomed to the javascript notation of arrays
- [[2023-12-26]]
	- [x] Add clear entry from local store button ✅ 2023-12-27
	- Added the bootstrap framework to make it look non-ugly
	- Can use plotly to chart my stuff?
		- [Getting started in JavaScript](https://plotly.com/javascript/getting-started/)
		- It's built on top of d3.js and seems easier to use. Can be added into my header to be called.
- [[2023-12-27]]
	- Nice got a decent version working so far
	- [x] Split out radar chart by emotion clusters (negative/positive/neutral/ambiguous) into 4 datasets ✅ 2023-12-28
	- [x] Human friendly timestamp readout for full day entry ✅ 2023-12-27
	- [x] Modify radar chart for legibility ✅ 2023-12-28

---

## Learned Lessons %% fold %%

---
> [!faq] What went well? What went poorly? What can we do better?

- Consider learning how to set up an app database and pushing date to it in a [[Interesting Project Ideas|future project]]
- Migrating to App Engine sinces [[Machine Learning|machine learning]] models require heavy memory usage and the low-cost [[Heroku|Heroku]] dynos are limited to 512mb ram
