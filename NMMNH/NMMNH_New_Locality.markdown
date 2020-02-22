### New Mexico Museum of Natural History and Science - Paleontology
# How To Create a New Locality

## Background 

Every cataloged item in the Paleontology collection at the New Mexico Museum of Natural History and Science (NMMNH) is associated with a numbered locality. Paleontological localities are often cited in literature, so the identifiers associated with localities are important. NMMNH locality numbers are placed in the LOCALITY NICKNAME field for each locality to allow ease of search for numbered localities. These identifiers are also included as a Site Identifier in the locality attributes for ease of public search.

Fossil poaching often occurs at paleontological sites. In order to prevent detailed information about the localities where NMMNH paleontological specimens were collected, specific locality information is obscured from public view through use of the access (private) locality attribute. For this reason, all NMMNH paleo specimens will have two specimen events, a public event which displays the public locality and a research event which includes all specific locality details. 

This documents the process for pre-creating named public and research localities to be used in data entry when new catalog records are added to the collection. In order to perform the tasks required, an Arctos user must have the [manage locality](http://arctos.database.museum/Admin/user_roles.cfm#manage_locality) role.

## Public Locality

To create the public locality, from the main menu select [Manage Data > Location > Find Locality](http://arctos.database.museum/Locality.cfm?action=findLO). 

### Clone a georeferenced county-level locality 

Public localities will not include any locality information other than higher geography and some locality attributes. In order to allow mapping of these "fuzzy" localities, it is important to start with a locality that has been georeferenced. If the new locality is within New Mexico or nearby states, it is likely that a georeferenced county locality already exists in Arctos. Cloning this to create the new locality will add consistency to the mapping of public localities. Begin with a search for a georeferenced county locality.

 - From the main Arctos menu select [Manage Data > Location > Find Locality](http://arctos.database.museum/Locality.cfm?action=findLO)
 - In the **Locality Nickname** field, enter the county for which you need a georeferenced locality in this format "State, County (no specific locality)". Quay County New Mexico will be entered as **New Mexico, Quay County (no specific locality)**
 - There should be only one result. If nothing is found, this means a georeferenced locality for the county you are using has not yet been created. **NEED INSTRUCTIONS FOR DOING THIS**
 - Select the "edit option for the locality.
 - **PLEASE DO NOT EDIT THE LOCALITY**, scroll to the bottom of the page and select "Clone Locality". This will preserve the pre-created georeferenced county for future use by yourself and other Arctos users.

### Edit Cloned locality

You now have a georeferenced, county-level locality that can be customized for NMMNH Paleo. To complete the customization edit the following fields:

 - **Locality Nickname** - this field will now appear as **clone of State, County (no specific locality)**, this should be deleted and the NMMNH Paleo locality entered in the format "NMMNH:Paleo:L-X_public" where X is the locality number. So locality 312 would be entered as **NMMNH:Paleo:L-312_public**.
 - **Specific Locality** - replace with **Specific locality encumbered** if something different is in the field.
 - **Locality Remarks** - delete anything in this field.
 
Once these edits are complete, scroll to the bottom of the page and select "Save Edits". Now the basic new locality has been created. The next step is to add Locality Attributes. Scroll to the bottom of the page again and you will see a box for "Geology Attributes. For each attribute described here, you will need to complete a new attribute box and save it by selecting "Create Determination". This adds the attribute to the locality with no need to re-save the locality itself. There are a few required attributes and many optional attributes.

#### Required Public Locality Attributes

**NMMNH Locality Number*** 
 - Attribute = Site Identifier
 - Value = NMMNH:Paleo:L-X (where X is the locality number)
 - Determiner = New Mexico Museum of Natural History and Science
 
**Site Found By** If more than one person found the site, add an attribute for each person. 
 - Attribute = Site Found By
 - Value = Arctos Agent name of person who found the site
 - Determiner = Arctos Agent name of person who found the site
 - Determined Date = Date the site was found in the format YYYY-MM-DD
 
**Site Found Date** 
 - Attribute = Site Found Date
 - Value = Date the site was found in the format YYYY-MM-DD
 - Determiner = Arctos Agent name of person who found the site
 - Determined Date = Date the site was found in the format YYYY-MM-DD
 
#### Optional Public Locality Attributes

**Site Identifier(s)** Paleo localities may have multiple identifiers. Enter as many as necessary.
 - Attribute = Site Identifier
 - Value = alphanumeric identifier as assigned
 - Determiner = Arctos Agent name of person who assigned the identifier (may be left blank)
 - Determined Date = Date the identifier was assigned in the format YYYY-MM-DD (may be left blank)
 
**Site Collector Number(s)** This should only be used for identifiers given to sites by the discoverer of the site, sites may have multiple discoveres, enter as many as necessary.
 - Attribute = Site Colelctor Number
 - Value = alphanumeric identifier as assigned
 - Determiner = Arctos Agent name of person who found the site
 - Determined Date = Date the site was found in the format YYYY-MM-DD
 
**Chronostratigraphy**
 - Attribute = Select appropriate term from code table. The most precise known level of chronostratigraphy should be chosen. Chronostratigraphy is hierarchical, so only the most precise value is required.
 - Value = Select from the code table
 - Determiner = Arctos Agent name of person who determined the chronostratigraphy (leave blank if unknown)
 - Determined Date = Date the determination was made in the format YYYY-MM-DD (leave blank if unknown)
 
**Lithostratigraphy** An attribute should be created for all given stratigraphic layers assigned.
- Attribute = Select appropriate term from code table
 - Value = Select from the code table
 - Determiner = Arctos Agent name of person who determined the lithostratigraphy (leave blank if unknown)
 - Determined Date = Date the determination was made in the format YYYY-MM-DD (leave blank if unknown)
 - Remark = lithostratigraphic description
 
**Biostratigraphy** An attribute should be created for all given stratigraphic layers assigned.
 - Attribute = Select appropriate term from code table
 - Value = Select from the code table
 - Determiner = Arctos Agent name of person who determined the biostratigraphy (leave blank if unknown)
 - Determined Date = Date the determination was made in the format YYYY-MM-DD (leave blank if unknown)
 
After all locality attributes in the categories above have been added to the new locality it is ready for use in cataloging and can be found easily using the locality nickname.

## Research Locality

To create the research locality, from the main menu select [Manage Data > Location > Find Locality](http://arctos.database.museum/Locality.cfm?action=findLO). 

### Clone the public locality 
 
All of the locality attributes created for the public locality will also be included in the research locality. Cloning the public locality will negate the need to create the public locality attributes for the research locality.

 - From the main Arctos menu select [Manage Data > Location > Find Locality](http://arctos.database.museum/Locality.cfm?action=findLO)
 - In the **Locality Nickname** field, enter the locality nickname for the public locality that was just created.
 - There should be only one result. If nothing is found, this means that either a public locality has not yet been created or it was not named appropriately. **NEED INSTRUCTIONS FOR DOING THIS**
 - Select the "edit option for the locality.
 - **PLEASE DO NOT EDIT THE LOCALITY**, scroll to the bottom of the page and select "Clone Locality". This will preserve the pre-created public locality for future use.

### Edit Cloned locality

You now have a locality with many of the attributes you will need that can be customized for the research locality. To complete the customization edit the following fields:

- **Higher Geography** - Many of the localities at the museum include the United States Geological Survet 7.5 minute topographic map (7.5 in map) designation. This designation provides a more refined higher geography than county alone. If a map designation is given for the locality, select "Change for this Locality", find the appropriate higher geography, and select "use this" to add it to the research locality.
- **Locality Nickname** - this field will now appear as **clone of NMMNH:Paleo:L-X_public** where X is the locality number. Edit this so that the NMMNH Paleo locality is entered in the format "NMMNH:Paleo:L-X" where X is the locality number. So locality 312 would be entered as **NMMNH:Paleo:L-312**
 - **Specific Locality** - replace **Specific locality encumbered** with the specific locality as given.
 - **Locality Remarks** - until locality attributes are created, the following ahould be added to locality remarks separated by a semicolon: accession number; UTM; species
 - **Coordinates** - if coordinates are provided, replace the county-level coordinates of the public locality with those given
 
Once these edits are complete, scroll to the bottom of the page and select "Save Edits". Now the basic new research locality has been created. The next step is to add research Locality Attributes. Scroll to the bottom of the page again and you will see a box for "Geology Attributes. For each attribute described here, you will need to complete a new attribute box and save it by selecting "Create Determination". This adds the attribute to the locality with no need to re-save the locality itself. There are a few required attributes and many optional attributes.

#### Required Public Locality Attributes

**Access*** 
 - Attribute = access
 - Value = private
 - Determiner = New Mexico Museum of Natural History and Science
 
#### Optional Research Locality Attributes

**Site Land Status** 
 - Attribute = Site Land Status
 - Value = select from the code table
 - Determiner = Arctos Agent name of person who determined the land staus of the site (leave blank if unknown)
 - Determined Date = Date the determination was made in the format YYYY-MM-DD (leave blank if unknown)
 - Remark = Name of map used to determine the land status
 
 **TRS Township** 
 - Attribute = TRS township
 - Value = select from the code table
 - Determiner = Arctos Agent name of person who determined the township (leave blank if unknown)
 - Determined Date = Date the determination was made in the format YYYY-MM-DD (leave blank if unknown)
 
**TRS Range** 
 - Attribute = TRS range
 - Value = select from the code table
 - Determiner = Arctos Agent name of person who determined the range (leave blank if unknown)
 - Determined Date = Date the determination was made in the format YYYY-MM-DD (leave blank if unknown)

**TRS Section** 
 - Attribute = TRS section
 - Value = select from the code table
 - Determiner = Arctos Agent name of person who determined the section (leave blank if unknown)
 - Determined Date = Date the determination was made in the format YYYY-MM-DD (leave blank if unknown)
 
 **TRS Aliquot** 
 - Attribute = TRS aliquot
 - Value = select from the code table
 - Determiner = Arctos Agent name of person who determined the aliquot (leave blank if unknown)
 - Determined Date = Date the determination was made in the format YYYY-MM-DD (leave blank if unknown)

After all locality attributes in the categories above have been added to the new locality it is ready for use in cataloging and can be found easily using the locality nickname.

---
title:NMMNH Paleontology How To Create a New Locality
layout: default_toc
author: Teresa J. Mayfield-Meyer
date: 2020-02-22
---
