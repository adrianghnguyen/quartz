---
dg-publish: true
aliases: Common luxon useful date formats
file-created: 2023-03-14
file-modified: 2023-05-05
tags: [computer-science/programming, computer-science]
linter-yaml-title-alias: Common luxon useful date formats
---

# Common luxon useful date formats

#status/done

Related to [[Working with dataview date tips]]

---

## Where to find the original source documentation for luxon date formats

Go here [formatting.md](https://raw.githubusercontent.com/moment/luxon/master/docs/formatting.md)

## Table of tokens

(Examples below given for `2014-08-06T13:07:04.054` considered as a local time in America/New_York).

| Standalone token | Format token | Description                                                    | Example                                                       |
| ---------------- | ------------ | -------------------------------------------------------------- | ------------------------------------------------------------- |
| S                |              | millisecond, no padding                                        | `54`                                                          |
| SSS              |              | millisecond, padded to 3                                       | `054`                                                         |
| u                |              | fractional seconds, functionally identical to SSS              | `054`                                                         |
| uu               |              | fractional seconds, between 0 and 99, padded to 2              | `05`                                                          |
| uuu              |              | fractional seconds, between 0 and 9                            | `0`                                                           |
| s                |              | second, no padding                                             | `4`                                                           |
| ss               |              | second, padded to 2 padding                                    | `04`                                                          |
| m                |              | minute, no padding                                             | `7`                                                           |
| mm               |              | minute, padded to 2                                            | `07`                                                          |
| h                |              | hour in 12-hour time, no padding                               | `1`                                                           |
| hh               |              | hour in 12-hour time, padded to 2                              | `01`                                                          |
| H                |              | hour in 24-hour time, no padding                               | `9`                                                           |
| HH               |              | hour in 24-hour time, padded to 2                              | `13`                                                          |
| Z                |              | narrow offset                                                  | `+5`                                                          |
| ZZ               |              | short offset                                                   | `+05:00`                                                      |
| ZZZ              |              | techie offset                                                  | `+0500`                                                       |
| ZZZZ             |              | abbreviated named offset                                       | `EST`                                                         |
| ZZZZZ            |              | unabbreviated named offset                                     | `Eastern Standard Time`                                       |
| z                |              | IANA zone                                                      | `America/New_York`                                            |
| a                |              | meridiem                                                       | `AM`                                                          |
| d                |              | day of the month, no padding                                   | `6`                                                           |
| dd               |              | day of the month, padded to 2                                  | `06`                                                          |
| c                | E            | day of the week, as number from 1-7 (Monday is 1, Sunday is 7) | `3`                                                           |
| ccc              | EEE          | day of the week, as an abbreviate localized string             | `Wed`                                                         |
| cccc             | EEEE         | day of the week, as an unabbreviated localized string          | `Wednesday`                                                   |
| ccccc            | EEEEE        | day of the week, as a single localized letter                  | `W`                                                           |
| L                | M            | month as an unpadded number                                    | `8`                                                           |
| LL               | MM           | month as a padded number                                       | `08`                                                          |
| LLL              | MMM          | month as an abbreviated localized string                       | `Aug`                                                         |
| LLLL             | MMMM         | month as an unabbreviated localized string                     | `August`                                                      |
| LLLLL            | MMMMM        | month as a single localized letter                             | `A`                                                           |
| y                |              | year, unpadded                                                 | `2014`                                                        |
| yy               |              | two-digit year                                                 | `14`                                                          |
| yyyy             |              | four- to six- digit year, pads to 4                            | `2014`                                                        |
| G                |              | abbreviated localized era                                      | `AD`                                                          |
| GG               |              | unabbreviated localized era                                    | `Anno Domini`                                                 |
| GGGGG            |              | one-letter localized era                                       | `A`                                                           |
| kk               |              | ISO week year, unpadded                                        | `14`                                                          |
| kkkk             |              | ISO week year, padded to 4                                     | `2014`                                                        |
| W                |              | ISO week number, unpadded                                      | `32`                                                          |
| WW               |              | ISO week number, padded to 2                                   | `32`                                                          |
| o                |              | ordinal (day of year), unpadded                                | `218`                                                         |
| ooo              |              | ordinal (day of year), padded to 3                             | `218`                                                         |
| q                |              | quarter, no padding                                            | `3`                                                           |
| qq               |              | quarter, padded to 2                                           | `03`                                                          |
| D                |              | localized numeric date                                         | `9/4/2017`                                                    |
| DD               |              | localized date with abbreviated month                          | `Aug 6, 2014`                                                 |
| DDD              |              | localized date with full month                                 | `August 6, 2014`                                              |
| DDDD             |              | localized date with full month and weekday                     | `Wednesday, August 6, 2014`                                   |
| t                |              | localized time                                                 | `9:07 AM`                                                     |
| tt               |              | localized time with seconds                                    | `1:07:04 PM`                                                  |
| ttt              |              | localized time with seconds and abbreviated offset             | `1:07:04 PM EDT`                                              |
| tttt             |              | localized time with seconds and full offset                    | `1:07:04 PM Eastern Daylight Time`                            |
| T                |              | localized 24-hour time                                         | `13:07`                                                       |
| TT               |              | localized 24-hour time with seconds                            | `13:07:04`                                                    |
| TTT              |              | localized 24-hour time with seconds and abbreviated offset     | `13:07:04 EDT`                                                |
| TTTT             |              | localized 24-hour time with seconds and full offset            | `13:07:04 Eastern Daylight Time`                              |
| f                |              | short localized date and time                                  | `8/6/2014, 1:07 PM`                                           |
| ff               |              | less short localized date and time                             | `Aug 6, 2014, 1:07 PM`                                        |
| fff              |              | verbose localized date and time                                | `August 6, 2014, 1:07 PM EDT`                                 |
| ffff             |              | extra verbose localized date and time                          | `Wednesday, August 6, 2014, 1:07 PM Eastern Daylight Time`    |
| F                |              | short localized date and time with seconds                     | `8/6/2014, 1:07:04 PM`                                        |
| FF               |              | less short localized date and time with seconds                | `Aug 6, 2014, 1:07:04 PM`                                     |
| FFF              |              | verbose localized date and time with seconds                   | `August 6, 2014, 1:07:04 PM EDT`                              |
| FFFF             |              | extra verbose localized date and time with seconds             | `Wednesday, August 6, 2014, 1:07:04 PM Eastern Daylight Time` |
| X                |              | unix timestamp in seconds                                      | `1407287224`                                                  |
| x                |              | unix timestamp in milliseconds                                 | `1407287224054`                                               |

## Most common luxon useful date formats

- [Website - Formatting in dateformats for Luxon](https://moment.github.io/luxon/#/formatting)
- [luxon/formatting.md at master · moment/luxon · GitHub](https://github.com/moment/luxon/blob/master/docs/formatting.md#presets)

### Common presets

Here's the full set of provided presets using the October 14, 1983 at `13:30:23` as an example.

> [!warning] You can't use this with dataview in Obsidian
> [[Working with dataview date tips]] <- Won't work
>
> Go here [[Common Luxon Useful Date Formats#Table of Tokens]]

| Name                         | Description                                                        | Example in en_US                                             | Example in fr                                              |
| ---------------------------- | ------------------------------------------------------------------ | ------------------------------------------------------------ | ---------------------------------------------------------- |
| `DATE_SHORT`                 | short date                                                         | `10/14/1983`                                                 | `14/10/1983`                                               |
| `DATE_MED`                   | abbreviated date                                                   | `Oct 14, 1983`                                               | `14 oct. 1983`                                             |
| `DATE_MED_WITH_WEEKDAY`      | abbreviated date with abbreviated weekday                          | `Fri, Oct 14, 1983`                                          | `ven. 14 oct. 1983`                                             |
| `DATE_FULL`                  | full date                                                          | `October 14, 1983`                                           | `14 octobre 1983`                                          |
| `DATE_HUGE`                  | full date with weekday                                             | `Friday, October 14, 1983`                                   | `vendredi 14 octobre 1983`                                 |
| `TIME_SIMPLE`                | time                                                               | `1:30 PM`                                                    | `13:30`                                                    |
| `TIME_WITH_SECONDS`          | time with seconds                                                  | `1:30:23 PM`                                                 | `13:30:23`                                                 |
| `TIME_WITH_SHORT_OFFSET`     | time with seconds and abbreviated named offset                     | `1:30:23 PM EDT`                                             | `13:30:23 UTC−4`                                           |
| `TIME_WITH_LONG_OFFSET`      | time with seconds and full named offset                            | `1:30:23 PM Eastern Daylight Time`                           | `13:30:23 heure d’été de l’Est`                            |
| `TIME_24_SIMPLE`             | 24-hour time                                                       | `13:30`                                                      | `13:30`                                                    |
| `TIME_24_WITH_SECONDS`       | 24-hour time with seconds                                          | `13:30:23`                                                   | `13:30:23`                                                 |
| `TIME_24_WITH_SHORT_OFFSET`  | 24-hour time with seconds and abbreviated named offset             | `13:30:23 EDT`                                               | `13:30:23 UTC−4`                                           |
| `TIME_24_WITH_LONG_OFFSET`   | 24-hour time with seconds and full named offset                    | `13:30:23 Eastern Daylight Time`                             | `13:30:23 heure d’été de l’Est`                            |
| `DATETIME_SHORT`             | short date & time                                                  | `10/14/1983, 1:30 PM`                                        | `14/10/1983 à 13:30`                                       |
| `DATETIME_MED`               | abbreviated date & time                                            | `Oct 14, 1983, 1:30 PM`                                      | `14 oct. 1983 à 13:30`                                     |
| `DATETIME_FULL`              | full date and time with abbreviated named offset                   | `October 14, 1983 at 1:30 PM EDT`                              | `14 octobre 1983 à 13:30 UTC−4`                            |
| `DATETIME_HUGE`              | full date and time with weekday and full named offset              | `Friday, October 14, 1983 at 1:30 PM Eastern Daylight Time`    | `vendredi 14 octobre 1983 à 13:30 heure d’été de l’Est`    |
| `DATETIME_SHORT_WITH_SECONDS`| short date & time with seconds                                     | `10/14/1983, 1:30:23 PM`                                     | `14/10/1983 à 13:30:23`                                    |
| `DATETIME_MED_WITH_SECONDS`  | abbreviated date & time with seconds                               | `Oct 14, 1983, 1:30:23 PM`                                   | `14 oct. 1983 à 13:30:23`                                  |
| `DATETIME_FULL_WITH_SECONDS` | full date and time with abbreviated named offset with seconds      | `October 14, 1983 at 1:30:23 PM EDT`                           | `14 octobre 1983 à 13:30:23 UTC−4`                         |
| `DATETIME_HUGE_WITH_SECONDS` | full date and time with weekday and full named offset with seconds | `Friday, October 14, 1983 at 1:30:23 PM Eastern Daylight Time` | `vendredi 14 octobre 1983 à 13:30:23 heure d’été de l’Est` |
