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

The "is_accepted_name" result indicates that the taxon name is in Arctos, it does not indicate whether or not the name has an associated classification. In order to ensure that names used by NMMNH Paleontology have approriate classifications, we performed the following steps for each is_accepted_name:

* Search for name in Arctos Taxonomy  
* If a classification is available in the Arctos taxonomy source, review for completeness. If the classification includes infromation for all appropriate higher classifications, author text, source, and taxon status, mark as complete. 
* If a classification is available in the Arctos taxonomy source, but it is missing information: review other classifications available in Arctos for the missing information and record it in the Excel sheet for addition to Arctos.  
* If a classification is available in the Arctos taxonomy source, but it is missing information and there are no other sources for it in Arctos: check for other similar names in Arctos Taxonomy (other names in the same genus could provide higher classification although not author text) and/or perform a Google search to look for possible classifications avialable elsewhere. Be extremely cautious and only use information from reputable sites. Always document sources.
* If a classification is not available in the Arctos taxonomy source: check for other similar names in Arctos Taxonomy (other names in the same genus could provide higher classification although not author text) and/or perform a Google search to look for possible classifications avialable elsewhere. Be extremely cautious and only use information from reputable sites. Always document sources.

