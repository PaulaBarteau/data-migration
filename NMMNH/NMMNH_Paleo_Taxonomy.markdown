---
title:NMMNH Paleontology Taxonomy Migration
layout: default_toc
author: Teresa J. Mayfield-Meyer
date: 2019-10-24
---

# NMMNH Paleontology Taxonomy Data Migration Documentation

## Background

The Paleontology collection at the New Mexico Museum of Natural History and Science (NMMNH) was previously managed in an MS Access database. The data was structured in several related tables, however, taxonomy was recorded directly in the SPECIMEN table. Every cataloged item in the SPECIMEN table included not only an identification, but all of that taxon's related higher classification information. This allowed for misspellings of determiniations as well as higher classification terms. In addition, modifers to the taxon names used in identification were placed directly in the taxon name field, resulting in multiple variations on many taxon names (Genus species sp., Genus species cf., Genus cf. species, Genus species nov., etc.). Identification terms (taxon names) are controlled in Arctos, this required a cleanup of taxon names in the MS Access data to remove extraneous modifications, correct misspellings, and locate and correct non-existant names.

## Taxon Names

After downloading names from the MS Access database to Excel, extraneous terms such as "sp.", "cf.", "nov.", etc. were removed from names, then duplicates were removed to create a list of unique names in use in the MS Access data. These names were run through the Arctos Scientific Name Checker tool. The output from the tool was separated into two sheets for further processing.

### is_accepted_name

The "is_accepted_name" result indicates that the taxon name is in Arctos, it does not indicate whether or not the name has an associated classification. In order to ensure that names used by NMMNH Paleontology have approriate classifications, we performed the following steps for each is_accepted_name:

* Search for name in [Arctos Taxonomy](http://arctos.database.museum/taxonomy.cfm) 
* If a classification is available in the Arctos taxonomy source, review for completeness. If the classification includes information for all appropriate higher classifications, author text, source, and taxon status, mark as complete. **[Abdounia](https://arctos.database.museum/name/Abdounia)** 
* If a classification is available in the Arctos taxonomy source, but it is missing information: review other classifications available in Arctos for the missing information and record it in the Excel sheet for addition to Arctos.   
* If a classification is available in the Arctos taxonomy source, but it is missing information and there are no other sources for it in Arctos: check for other similar names in Arctos Taxonomy (other names in the same genus could provide higher classification although not author text) and/or perform a Google search to look for possible classifications avialable elsewhere. Be extremely cautious and only use information from reputable sites. Always document sources. 
* If a classification is not available in the Arctos taxonomy source: check for other similar names in Arctos Taxonomy (other names in the same genus could provide higher classification although not author text) and/or perform a Google search to look for possible classifications avialable elsewhere. Be extremely cautious and only use information from reputable sites. Always document sources. 

### FAIL

The "FAIL" result indicates that the taxon name is not in Arctos. There may be many reasons for this such as the name is misspelled (either in the MS Access data or Arctos), the name is not properly formatted, the name is not accepted, or simply that the name has never been used by an Arctos collection (and therefor has not been added to Arctos taxon names). In order to ensure that names used by NMMNH Paleontology meet current taxonomic standards, we performed the following steps for each FAIL: 

* Run the list of FAIL taxon names through the [Taxon Name Validator](http://arctos.database.museum/DataServices/taxonNameValidator.cfm). This helped to prioritize names that might be easier to research. Names with "found" in more than one of the resources are more likely to be valid and just missing from Arctos rather than a misspelling, but always double check! 

* For binomial and trinomial names, search the genus in Arctos. 
  If the genus is in Arctos, check for alternate spellings of the specific epithet. If a misspelling is indicated because an alternate spelling is in Arctos, check elsewhere to ensure that the Arctos spelling is correct as incorrectly spelled names can make their way into Arctos. Once it is determined which spelling is correct, make a note to either correct the spelling in the MS Access data or to add the correct spelling to Arctos. (If the second, and others have used the misspelled name, please leave an annotation on the taxon by selecting the "comment/report bad data" button at the top of the taxon page). 
  If the genus is not in Arctos, search the resource where the name was found. Use jusdgement based upon the information at the resource to determine if the name should be added to Arctos, the spelling in the MS Access data should be corrected, or some other action is required.

* For monomial names, search the resource where the name was found. Use judgement based upon the information at the resource to determine if the name should be added to Arctos, the spelling in the MS Access data should be corrected, or some other action is required.

