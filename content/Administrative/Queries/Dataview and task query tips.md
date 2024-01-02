---
aliases:
  - Dataview and task query tips
  - dataview tips
  - Obisidian data query tips
  - Obsidian queries
  - task query Obsidian
  - task query
tags:
  - admin/query
note-type: 
description: 
file-created: 2023-02-27
file-modified: 2023-11-14
doc-type: 
linter-and task yaml-title-alias: Dataview query tips
---

# Dataview and task query tips

#status/wip

[GitHub - s-blu/obsidian\_dataview\_example\_vault: A example vault to collect and showcase various dataview queries. Created on behalf of AB1908](https://github.com/s-blu/obsidian_dataview_example_vault)

## Query Types

- <https://blacksmithgu.github.io/obsidian-dataview/queries/query-types/>
- List
- Table
	- Use "Without ID" if you don't want header
- Task

## Task search

Task search in current file
```
tasks  
not done
path includes {{query.file.path}}
```
the `{{query.file.path}}` aliases to the current directory. See [Filters - Tasks User Guide - Obsidian Publish](https://publish.obsidian.md/tasks/Queries/Filters#File%20Path)


## Pulling bulletpoints under headings

 FLATTEN file.lists as bullets: file.lists is "A list of all list elements in the file", see https://blacksmithgu.github.io/obsidian-dataview/annotation/metadata-pages/.
>
> file.lists is an array of items and FLATTEN "flatten"s it out so that each item in the array can be treated as a separate row, see next.
>
> LIST rows.bullets.text: these are the rows, aka list items. We want to LIST the text object of the bullets object of each row.
>
> But now we want to filter what "rows" aka list items we want to display: the meta function is used to access metadata about the bullet items. meta(bullets.section) accesses metadata of the section that contains the bullets and we filter only those within a subsection named "Journal".
> 


```
LIST rows.bullets.text
FLATTEN file.lists as bullets
WHERE week = "2023-W45" AND meta(bullets.section).subpath = "Journal"
SORT file.name desc
GROUP BY file.name
```



## Working with dates

Obtain all files which were modified in the last 24 hours
`LIST WHERE file.mtime >= date(today) - dur(1 day)`

Find all projects which are not marked complete and are more than a month old:
`LIST FROM #projects WHERE !completed AND file.ctime <= date(today) - dur(1 month)`

### Subtracting or adding durations on dates

[Literals - Dataview](https://blacksmithgu.github.io/obsidian-dataview/reference/literals/#dates)

```
	WHERE date(today)-dur(3 months) < file-created
	SORT file-created
```
Example where I am looking at the last 3 months by subtracting a duration object

`date(today) - dur(1 mo) < date(file.name) as "Last month"` <- Return the notes where the title is within the last 30 days

### Displaying date within a certain format

Note: It uses luxon
``dateformat(file-created,"MMMM yyyy") as "Month",``


For daily journal notes, you can use the title as the date field
`date(file.name)` will parse `2023-08-28` into `August 28, 2023` correctly
## Query structures

Metadata Filtering Goes in the WHERE Clause

```
WHERE metadataKey %%Checks for existence%%
WHERE metadataKey = blahblah
```

 Ignore File Path in DQ or exclude path

```
WHERE !contains(file.path, "Templates")
```

### How to List All Links to Current File

```dataview
list 
from [[]]
SORT file.cday DESC
```

## Using in-line dataview

[Adding Metadata - Dataview](https://blacksmithgu.github.io/obsidian-dataview/annotation/add-metadata/)

- `[rating:: 9]`
- `Basic Field:: Some random Value`
- `(longKeyIDontNeedWhenReading:: key)`

You can't see it under but it's an inline dataview *"=this.file.name"*
`= this.file.name` it's a query on the properties of the current file

### How to use dataquery to retrieve deep attributes through metadata

This query below can retrieve nested file attributes as long as the YAML fields were well-defined. Perhaps I can use this for people attributes. They can be chained.

```
`=this.target_character.parent.parent.spouse.birth_place.date_founded`
```

> [!NOTE]- Original post
> No problem.
> 
> > wouldn't that support the point of using atomic notes and its links within the body rather than putting it in the header?
> 
> If you're just using links, there's no context to them.
> 
> You might have a dozen links in a character file -- links to related subjects (perhaps an explanation of a sport or scientific process that's mentioned in their backstory), links to their parents, links to locations they've lived in, links to close friends, links to major life events… How do you know which is their birthplace amongst all those links?
> 
> That's what metadata is for. It's data that describes the data itself, so you know what you're working with and can locate information without having to physically be in the source files looking for context clues.
> 
> (The benefit of being able to put it in YAML instead of just using inline Dataview is that YAML is a more standard format for metadata. So other programs are more likely to support it, and it's easier for you to build over if you like to code.)
> 
> > perhaps seeing the code for your example of "the founding date of the birthplace from the parents' parents' spouses' notes"?
> >
> 
> For this fun but admittedly not super practical example:
> 
> ```
> `=this.target_character.parent.parent.spouse.birth_place.date_founded`
> ```
> 
> spits out the years/dates in question with Dataview.
> 
> This involves a `target_character:: [[the main character]]` key in the current file (could alternatively use `this.file.link`), then in that file a `parent:: [[their parent]]`, then in those parent files `parent:: [[the parent's parent i.e. the target's grandparent]]`, then in those files `spouse:: [[the grandparent's spouse]]` (possibly the same people, possibly not), then in those files a `birth_place:: [[location those characters were born in]]`, then in the birth location files finally a `date_founded:: 1628 or whatever`.
> 
> (You'd repeat the keys as many times as they're needed, like most characters would have two `parent::` keys. Dataview automatically grabs all of them when querying.)
> 
> e: Even if you want to get super atomic so that there are as few links and keys as possible in each note -- say, having character files broken down so there's a character description file and a character backstory file etc -- you can still use this method there. `target_character.description.appearance.height`.
> 
> A strict naming convention could also work (`[[chr60_description_appearance]].height`) ofc, but it's messier (on the automation side) than working with everything as separate objects.