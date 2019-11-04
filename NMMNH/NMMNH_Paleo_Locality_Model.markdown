---
title:NMMNH Paleontology Locality Model and Data Migration
layout: default_toc
author: Teresa J. Mayfield-Meyer
date: 2019-10-22
---
# NMMNH Paleontology Locality Model and Data Migration

## Background

The Paleontology collection at the New Mexico Museum of Natural History and Science (NMMNH) was previously managed in an MS Access database. The data was structured in several related tables, including LOCALITY and SPECIMEN. Every cataloged item in the SPECIMEN table included a reference to numbered locality in the LOCALITY table. Paleontological localities are often cited in literature, so the identifiers associated with localities are important. It was determined that the NMMNH locality numbers would be placed in the [LOCALITY NICKNAME](http://handbook.arctosdb.org/documentation/locality.html#locality-nickname) field for each locality to allow ease of search for numbered localities.

In some cases, localities were re-visited, resulting in multiple collecting events for those localities. It was determined that each event would be given an identifier that included the LOCALITY NICKNAME appended with a dash and a sequential number and that this identifier would be placed in the [COLLECTING EVENT NICKNAME](https://handbook.arctosdb.org/documentation/collecting-event.html#event-nickname) field for each collecting event.

Fossil poaching often occurs at paleontological sites. In order to prevent detailed information about the localities where NMMNH paleontological specimens were collected, it was determined that specific locality information should be obscured from public view.  At the time these records were being migrated, there was no encumbrance model for an entire locality. With help from the Arctos DBA, we devised a ssystem to allow us to hide the "research locality" from public view and create a second "public locality" that would display to anyone without appropriate access to the NMMNH:Paleo collection.

Many of the localities at the museum include the United States Geological Survet 7.5 minute topographic map (7.5  in map) designation. This designation provides a more refined higher geography than county alone, so it was decided that all of the 7.5 min maps would be added to higher geography. Using [The National Geologic Map Database](https://ngmdb.usgs.gov/topoview/viewer/#4/39.98/-100.06), a student completed a higher geography upload template with links to USGS topographic maps that added approximately 2,400 unique higher geography entries for County/Quad combinations in Arctos which allowed us to provide a more refined higher geography for the museum's paleo localities.

This documents the process for pre-creating named "research localities" and associating them with object records in Arctos that were loaded with "public localities".

## Bulkloading Named Localities

There is not a tool for bulkloading localities. Using the terms included in a locality, a [template](https://github.com/ArctosDB/data-migration/blob/master/Templates/LOCALITY_BULKLOAD.csv) was created that would allow for bulkloading. Once the data was entered into the template, it was saved as a CSV and sent to the Arctos DBA for upload.

### Encumbering Named Localities and Related Collecting Events

To facilitate encumbering an entire locality and its related collecting events, a new [GEOLOGY_ATTRIBUTE](http://arctos.database.museum/info/ctDocumentation.cfm?table=CTGEOLOGY_ATTRIBUTE) "access" with the value "private" was created. Assigning the private (access) GEOLOGY_ATTRIBUTE to any locality hides the locality and any related events from public view in any specimen record using the locality as well as the [Places search](http://arctos.database.museum/showLocality.cfm). We added the private (access) GEOLOGY_ATTRIBUTE to all named localities to create a "research locality" that is only available to Arctos users assigned access to the NMMNH:Paleo collection.

## Bulkloading Named Collecting Events

There is not a tool for bulkloading collecting events. Using the terms included in a collecting event, a [template](https://github.com/ArctosDB/data-migration/blob/master/Templates/COLL_EVENT_BULKLOAD.csv) was created that would allow for bulkloading. The locality information for each event was selected using the appropriate locality name in the LOCALITY_NICKNAME field. Once the data was entered into the template, it was saved as a CSV and sent to the Arctos DBA for upload.

## Bulkloading Object Records

Using the [Bulkload Records](https://arctos.database.museum/Bulkloader/BulkloadSpecimens.cfm) tool, we created a bulkload using only the Higher Geography from the related LOCALITY_NICKNAME for locality. This will create a very spare, public locality for all paleo records.

## Adding Named Collecting Events to Object Records

Using the [Specimen Event Bulkload Tool](http://arctos.database.museum/tools/BulkloadSpecimenEvent.cfm) we created a bulkload to add an event to each loaded object record using the COLLECTING_EVENT_NICKNAME to associate the research locality information with each object record.
