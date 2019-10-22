---
title:How To Migrate Data Into Arctos Using Named Localities and Collecting Events
layout: default_toc
author: Teresa J. Mayfield-Meyer
date: 2019-10-22
---
# How To Migrate Data Into Arctos Using Named Localities and Collecting Events

## Background

The Paleontology collection at the New Mexico Museum of Natural History and Science (NMMNH) was previously managed in an MS Access database. The data was structured in several related tables, including LOCALITY and SPECIMEN. Every cataloged item in the SPECIMEN table included a reference to numbered locality in the LOCALITY table. Paleontological localities are often cited in literature, so the identifiers associated with localities are important. It was determined that the NMMNH locality numbers would be placed in the [LOCALITY NICKNAME](http://handbook.arctosdb.org/documentation/locality.html#locality-nickname) field for each locality to allow ease of search for numbered localities.

In some cases, localities were re-visited, resulting in multiple collecting events for those localities. It was determined that each event would be given an identifier that included the LOCALITY NICKNAME appended with a dash and a sequential number and that this identifier would be placed in the [COLLECTING EVENT NICKNAME](https://handbook.arctosdb.org/documentation/collecting-event.html#event-nickname) field for each collecting event.

This How To documents the process for pre-creating named localities and collecting events and using them to load object records into Arctos.

## Bulkloading Named Localities

There is not a tool for bulkloading localities. Using the terms included in a locality, a [template](https://github.com/ArctosDB/data-migration/blob/master/Templates/LOCALITY_BULKLOAD.csv) was created that would allow for bulkloading. Once the data was entered into the template, it was saved as a CSV and sent to the Arctos DBA for upload.

## Bulkloading Named Collecting Events

There is not a tool for bulkloading collecting events. Using the terms included in a collecting event, a [template](https://github.com/ArctosDB/data-migration/blob/master/Templates/COLL_EVENT_BULKLOAD.csv) was created that would allow for bulkloading. The locality information for each event was selected by using the LOCALITY_NICKNAME field. Once the data was entered into the template, it was saved as a CSV and sent to the Arctos DBA for upload.

## Bulkloading Object Records

Using the [Bulkload Records](https://arctos.database.museum/Bulkloader/BulkloadSpecimens.cfm) tool, we were able to create a bulkload using only the COLLECTING_EVENT_NICKNAME field to add all event and locality information to each object record.