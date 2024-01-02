---
aliases:
  - Bikeshare data
  - rideshare data
tags:
  - society/city/urban-planning
  - computer-science/data
  - hobbies/cycling
file-created: 2023-05-09
file-modified: 2023-09-02
note-type: general
description: 
linter-yaml-title-alias: Bikeshare data
---

# Bikeshare data

#status/postponed

---

[Open Data | BIXI Montréal](https://bixi.com/en/open-data)

## Biki station feed

Format feed standard

[GitHub - MobilityData/gbfs: ❗️Now hosted by MobilityData❗️ Documentation for the General Bikeshare Feed Specification, a standardized data feed for shared mobility system availability.](https://github.com/MobilityData/gbfs)

```
{"last_updated":1683635762,"ttl":10,"data":{"en":{"feeds":[{"name":"station_status","url":"https://gbfs.velobixi.com/gbfs/en/station_status.json"},{"name":"system_alerts","url":"https://gbfs.velobixi.com/gbfs/en/system_alerts.json"},{"name":"system_information","url":"https://gbfs.velobixi.com/gbfs/en/system_information.json"},{"name":"station_information","url":"https://gbfs.velobixi.com/gbfs/en/station_information.json"}]},"fr":{"feeds":[{"name":"station_status","url":"https://gbfs.velobixi.com/gbfs/fr/station_status.json"},{"name":"system_alerts","url":"https://gbfs.velobixi.com/gbfs/fr/system_alerts.json"},{"name":"system_information","url":"https://gbfs.velobixi.com/gbfs/fr/system_information.json"},{"name":"station_information","url":"https://gbfs.velobixi.com/gbfs/fr/station_information.json"}]}}}
```

## My Bike Traffic

[MyBikeTraffic.com MyBikeTraffic.com - Home](https://www.mybiketraffic.com/)

This is a website which gets information from Garmin Varias and but there seems to be no APIs. The professor running it may be open to sharing his data? We'd have to see. It monitors car traffic information.

It could be an interesting [[data source for projects|data source for projects]].

## Montreal Open Bike Ridership data

This is the dataset for Montreal bike counters. Unfortunately, it seems like the data was not well standardized in prior years which makes longitudinal studies a bit difficult based on some people's comments.

It could make an [[Interesting Project Ideas|interesting project]] to see polish and clean up the data.

[Comptages des vélos sur les pistes cyclables - Site web des données ouvertes de la Ville de Montréal](https://donnees.montreal.ca/dataset/velos-comptage#data)


[Traffic flow information](https://www150.statcan.gc.ca/n1/pub/71-607-x/71-607-x2022018-eng.htm) There doesn't seem to be any good proxies for accurate car counts except things which are camera-based. The government of Canada has a visual estimation methods and there data source can be found here
- [Download traffic information](https://www150.statcan.gc.ca/pub/71-607-x/2022018/tf-ft-eng.csv)

