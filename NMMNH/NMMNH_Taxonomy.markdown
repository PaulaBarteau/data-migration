---
title:NMMNH Paleontology Taxonomy Migration
layout: default_toc
author: Teresa J. Mayfield-Meyer
date: 2019-10-24
---
# NMMNH Paleontology Taxonomy Data Migration Documentation

## Background

The Paleontology collection at the New Mexico Museum of Natural History and Science (NMMNH) was previously managed in an MS Access database. The data was structured in several related tables, including TAXA and SPECIMEN. Every cataloged item in the SPECIMEN table included a reference to numbered locality in the LOCALITY table. Paleontological localities are often cited in literature, so the identifiers associated with localities are important. It was determined that the NMMNH locality numbers would be placed in the LOCALITY NICKNAME field for each locality to allow ease of search for numbered localities.

## Taxon Names

After downloading names from the MS Access database to Excel, extraneous terms such as "sp.", "cf.", "nov.", etc. were removed from names, then duplicates were removed to create a list of unique names in use in the MS Access data. These names were run through the Arctos Scientific Name Checker tool. The output from the tool was separated into two sheets for further processing.

### is_accepted_name


