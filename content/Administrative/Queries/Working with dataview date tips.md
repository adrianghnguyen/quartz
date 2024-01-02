---
doc-type: 
aliases: Working with Dataview Dates
linter-yaml-title-alias: Working with Dataview Dates
tags: [admin/query, admin/obsidian-management]
file-created: 2023-03-14
file-modified: 2023-03-16
---

# Working with Dataview Dates

---

## Dataview Field Properties

[Data Types - Dataview](https://blacksmithgu.github.io/obsidian-dataview/annotation/types-of-metadata/#date)

- Use luxon tokens

> Displaying of date objects
>
> Dataview renders date objects in a human readable format, i.e. `3:15 PM - Februar 26, 2021`. You can adjust how this format looks like in Dataview's Setting under "General" with "Date Format" and "Date + Time Format". If you want to adjust the format in a specific query only, use the [dateformat function](https://blacksmithgu.github.io/obsidian-dataview/reference/functions/#dateformatdatedatetime-string).

### Available Fields

> -   field.year
> -   field.month
> -   field.weekyear
> -   field.week
> -   field.weekday
> -   field.day
> -   field.hour
> -   field.minute
> -   field.second
> -   field.millisecond

## Using Dateformat Function

[Functions - Dataview](https://blacksmithgu.github.io/obsidian-dataview/reference/functions/#dateformatdatedatetime-string)

General form: `dateformat(date|datetime, string)`

```js
dateformat(file.ctime,"yyyy-MM-dd") = "2022-01-05"
dateformat(file.ctime,"HH:mm:ss") = "12:18:04"
dateformat(date(now),"x") = "1407287224054"
dateformat(file.mtime,"ffff") = "Wednesday, August 6, 2014, 1:07 PM Eastern Daylight Time"
dateformat(file.mtime,"ffff") = "Wednesday, August 6, 2014, 1:07 PM Eastern Daylight Time"
```
Use these with dataview.

![[Common Luxon Useful Date Formats#Table of Tokens]]

## Date Object Literal

- [Literals - Dataview](https://blacksmithgu.github.io/obsidian-dataview/reference/literals/#dates)
- See also [[Literals]]
