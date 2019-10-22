---
title:How To Migrate Data Into Arctos Using Named Localities and Collecting Events
layout: default_toc
author: Teresa J. Mayfield-Meyer
date: 2019-10-22
---
# How To Migrate Data Into Arctos Using Named Localities and Collecting Events

## Background

The Paleontology collection at the New Mexico Museum of Natural History and Science (NMMNH) was previously managed in an MS Access database. The data was structured in several related tables, one of which was LOCALITY. Every cataloged item in the SPECIMEN table included a reference to numbered locality in the LOCALITY table. Paleontological localities are often cited in literature, so the identifiers associated with localities are important. It was determined that the NMMNH locality numbers would be placed in the LOCALITY NICKNAME field for each locality to allow ease of search for numbered localities.

In some cases, localities were re-visited, resulting in multiple collecting events for those localities. It was determined that each event would be given an identifier that included the LOCALITY NICKNAME appended with a dash and a sequntial number and that this identifier would be placed in the COLLECTING EVENT NICKNAME field for each collecting event.

This How To documents the process for pre-creating named localities and collecting events and using them to load object records into Arctos.

## Bulkloading Named Localities

There is not a tool for bulkloading localities. Using the terms included in a locality, a template was created that would allow for bulkloading. Once the file was complete, it was saved as a CSV and sent to the Arctos DBA for upload.

