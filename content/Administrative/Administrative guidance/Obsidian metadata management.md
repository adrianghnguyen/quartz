---
aliases:
  - Obsidian metadata management
  - pkm data management
  - Obsidian metadata
tags:
  - admin
note-type:
  - 
description: 
file-created: 2023-08-30
file-modified: 2023-11-04
linter-yaml-title-alias: Obsidian metadata management
topic:
  - 
---

# Obsidian metadata management

#status/wip

---

> [!Info] See also [[Templater tips and tricks|Templater Tips and Tricks]]

## Cleaning up my metadata

- Review templates ➕ 2023-09-01
- Flatten tags and combine redundant ones
- Review properties pane to remove redundant or combine
- Fold `#admin/moc` into `#admin/moc`? Think about this for a bit. Same for `#folder` into `#admin/folder`

guess I already have `#admin` with its children tag which I can filter from dataquery

Bring `#admin/moc` into its `#admin/moc`? It would allow when making searching in graph view to just filter out anything that's `#admin`

- What do folders have? they're tagged with `#folder` so I could bring them into `#admin/folder`
	- If I do that, need to change the templates accordingly for new folder notes.

What are some of the fields I would like to hold in [[Dataview and task query tips|my dataview queries]]?

| Attribute                  | Property | Explanation |
| -------------------------- | -------- | ----------- |
| Hide from dataview queries | dataview-hide         |             |

## Standard fields

Fields I wish to standardize upon

- progress
	- backlog
	- upcoming
	- in progress
	- paused
	- completed
	- dropped
- start
	- date field
- end
	- also used on behalf of completed
	- date field
- description
	- used for summaries, additional notes or whatever to surface
- note-type (list type) <- indicates the nature of the note
	- project
	- reference <- anything related youtube, etc.
	- book
	- home
	- diary
	- education
	- assessment
	- administrative <- obsidian management junk
- topic
	- generic field
	- Can be used in notes for the scientific area of research or whatever.
	- In home notes, it can indicate finance, insurance, purchase, etc.
- priority
	- high
	- medium
	- low
- importance
	- high
	- medium
	- low
- objective
	- can be used for personal people goals but also myself in my monthly notes
	- generic text field

Priority and importance are pulled concepts from the [[Use the Eisenhower decision matrix to triage decisions|Eisenhower decision matrix]].

### General notes

- [x] Refactor ➕ 2023-09-01 ✅ 2023-12-12

Fields I want to share across all my notes will go into linter?
- note-type
- topic
- file-created
- file-modified
- description
- type???

Used `#assessment` for personal surveys and stuff? Might be the better option rather than putting it into the metadata
- [x] Move assessment into tags ➕ 2023-09-01 ✅ 2023-12-12
- [x] Create metadata property ✅ 2023-12-12

### Home management

- [x] Refactor ➕ 2023-09-01 ✅ 2023-12-12
- [x] modify template ✅ 2023-12-12

- location
	- current address of the home
- note-type: household
- topic
	- tax
	- home-improvement
	- medical
	- insurance
	- purchase
	- finance

### Diary

- [x] Refactor ➕ 2023-09-01 ✅ 2023-12-12
- [x] modify template ✅ 2023-09-01

- location
	- Where I was during that day
- importance
	- high <- big day
	- medium <- general
	- low <- trivial or non-eventful day
- event
	- tracked as dataview in line
- mood
- sleep
- meditation
- exercise
	- [x] rename physical-activity to exercise ➕ 2023-09-01 ✅ 2023-09-12

### People

- [x] Refactor ➕ 2023-09-01 ✅ 2023-12-12
- [x] modify template to add in new fields ✅ 2023-09-01
- [x] Simplify template if possible? ✅ 2023-09-01

- introduction <- how we met
- start <- first meeting date, repurposing from generic
- birthday
- significant date
- company
- occupation
- relationship
- goals
- likes
- dislikes
- contact -> how to contact them
- hobbies

### Books

- [x] Refactor ➕ 2023-09-01 ✅ 2023-12-12
- [x] modify template ✅ 2023-12-12

- start
- end
- progress
- topic
- author

- [x] Refactor ➕ 2023-09-01 ✅ 2023-12-12
- [x] modify template ✅ 2023-12-12
- [x] RF total -> page-total ✅ 2023-12-12

### Projects

- start
	- generic field repurposed
- end
	- generic field repurposed
- complexity
- importance
- priority
- description <- generic field repurposed

## References notes from readit later

- [x] Reference notes need to be merged into note-type: reference ✅ 2023-12-12
- [x] simplify the template right now there's a lot of bullshit fluff ✅ 2023-12-12
- [x] remove the dataview ✅ 2023-12-12

- type:
	- the media source such as YT, twitter, etc.
- author
- location
	- url and shit
