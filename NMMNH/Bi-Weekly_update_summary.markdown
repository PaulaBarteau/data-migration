# NMMNH Digitization Project Completed Bi-Weekly Summary Items

This document lists major tasks completed by the team over the course of the project as reported in the Weekly Meeting notes.

## Progress Report

On Monday, April 13, the production instance of Arctos went down. Covid-19 restrictions meant that tech support from TACC could not access the system until the following day. Repair of the Oracle box is under way. In the mean time, searches could be made on the ArctosPG test version at http://test.arctos.database.museum

On Tuesday, April 28, the production instance of Arctos was restored, but with the last available recoverable back-up from March 15, 2020. Numbers with lines through them represent data before the crash and numbers without a line represent current data.

Total records in Arctos: ~56,760~ 104,872  
Images Taken: 51  
Taxa added to Arctos: ~327~ ?  
Classifications added to Arctos: ~555~ ?  
Publications added to Arctos: ~10~ ?  

### Geoscience Migration Stats  

Stat | Records	| % Complete 
-- | -- | --
Total Specimen Records	| 80,901 |	
No data records	| (1,966)	| -2% | 
**Total records to migrate**	| **78,940** | 	
Records in Arctos	| ~41,646~ 71,680 |	~51%~ 91%
Not yet loaded	| ~25,282~ 9,860 |	~31%~ 9%
Locality Issues (unable to load)	| 0 |	0%
*Records with Research Events*	| ~40,126~ 42,293 |	~50%~ 53.5%
**Total Localities**	| **12,345** |	
Research Localities Loaded	| 12,345 |	100%
Locality Issues (unable to load)	| 0 |	0%
*Specimen-less localities*	| 3,732 |	30%

## Completed by Person

### Geoscience

#### Teresa
##### Benefits all Arctos Collections
 - Added 30 features and created 40 new higher geography entries
 - wrote [How To Create a Locality](http://handbook.arctosdb.org/how_to/How-to-Create-a-Locality.html)
 - wrote [How to Encumber Locality Data](http://handbook.arctosdb.org/how_to/How-to-Encumber-Locality.html)
 - Wrote [How To Add Geology Attributes to a Locality](http://handbook.arctosdb.org/how_to/How-to-Add-Geology-Attributes-to-a-Locality.html)
 - Updated "[How to Manage a Collection](http://handbook.arctosdb.org/how_to/How-to-Manage-a-Collection-in-Arctos.html)" for the Arctos community.
 - Wrote - [How to Bulkload Media Metadata](http://handbook.arctosdb.org/how_to/How-to-Bulkload-Media-Metadata.html)
 - Added definitions to 68 Chronostratigraphy - International Commission on Stratigraphy terms in the [geology code table](http://arctos.database.museum/info/ctDocumentation.cfm?table=CTGEOLOGY_ATTRIBUTE).
 - Added 58 Chronostratigraphy - International Commission on Stratigraphy terms (all terms from Phanerozoic to present) to the [geology code table](http://arctos.database.museum/info/ctDocumentation.cfm?table=CTGEOLOGY_ATTRIBUTE).
 - Created video tutorial for uploading small batches of media to TACC
 - Created video tutorial for bulkloading media metadata
 - Bulkloaded 245 Geology Attribute terms to be used as new locality attributes.
 - Added definitions for 108 part names in the <a href="https://arctos.database.museum/info/ctDocumentation.cfm?table=CTSPECIMEN_PART_NAME">Arctos Part Name Code Table<a/>.
 - Worked with Arctos programmer to create a new method for encumbering all locality data.
 - Assisted with migration of Arctos from Oracle to PostgreSQL 
   
##### Benefits NMMNH Geoscience
 - Completed "Manage Collection" for Paleo and Geol adding museum logo to record header and details for future publication to aggregators. 
 - Tested bulkload of research localities and collecting events with Arctos programmer. 
 - Bulkloaded 42,293 specimen records with public and research events 
 - Bulkloaded 115 non-conforming Agents to Arctos 
 - Bulkloaded 12,345 research localities to Arctos 
 - Bulkloaded 12,345 public localities to Arctos 
 - Normalized and sent 604 "Site Found By" locality attributes to Arctos DBA for upload 
 - Normalized and sent 2,482 "Site Found Date" locality attributes to Arctos DBA for upload 
 - Normalized and sent 12,188 "Site Identifier" locality attributes to Arctos DBA for upload 
 - Normalized and sent 478 "TRS Aliquot" locality attributes to Arctos DBA for upload 
 - Acquired paleo imaging protocols/workflows from Yale Peabody - stored in N:\GeoScience\Arctos\Imaging 
 - Claimed barcodes for all collections: NMMNH followed by up to 12 numeric or text characters plus _ or - 
 - [Written procedures for creating localities](https://github.com/ArctosDB/data-migration/blob/master/NMMNH/NMMNH_New_Locality.markdown) 
 - reviewed 459 non-conforming taxon names 
 - Created [Google form](https://docs.google.com/forms/d/18NnbuItBYoY3m8m-B-PQMguOOxpK1Qx7BJ9L7BwrAMY/viewform?edit_requested=true) for capturing publication information. 
 - Presented [Data Management Strategies for the Extended Specimen](https://github.com/ArctosDB/SPNHC/issues/33#issuecomment-586483125) at virtual SPNHC Symposium
 
#### Nicole
##### Benefits all Arctos Collections 
 - Created the bulkload for 115 non-conforming Agent names 
 - Since beginning of project has created 530 agents in Arctos (256 bulkloaded, 274 entered individually) 
 - Researched and provided information for 66 geology terms 

##### Benefits NMMNH Geoscience
 - Reviewed and provided corrected higher geography for 544 localities 
 - Reviewed and provided corrected Faunal Zones for 537 localities 
 - Reviewed and provided corrected Stratigraphic data for 309 localities 
 - Researched and corrected geology attributes for 2,416 localities 
 - Reviewed and provided standardized names for 1,860 parts 
 
#### Hannah
##### Benefits all Arctos Collections
 - 283 taxa/classifications added to Arctos
 - 2,695 higher geography quad maps compiled for bulkload
 - Researched geology terms 148-433
 - Scale rulers for imaging printed out at UPS and ready for when imaging can continue
 - 2,620 mineral taxonomy links compiled
 
#### Benefits NMMNH Geoscience
- Wrote and submitted Gila Symposium abstract- "Sharing Paleontology of the Gila at New Mexico Museum of Natural History and Science"
- Presentation at Gila Symposium "[Sharing Paleontology of the Gila at New Mexico Museum of Natural History and Science](http://arctos.database.museum/project/10003333)"
 - Imaging equipment set up and working properly
 - First two images taken of holotpyes
 - Progress with social media posts and plans with curators for their engagement in social media
 - Checked on discrepancies between 10 records in Arctos and records in MS Access data
 - Twitter post written about the Oreodont
 - 1,800 mineral localities complete 
 - Twitter post written for Fossil Friday
 - Wrote article for Black Range Naturalist

#### Lucius
##### Benefits all Arctos Collections
- Created defintions for 108 part names in the <a href="https://arctos.database.museum/info/ctDocumentation.cfm?table=CTSPECIMEN_PART_NAME">Arctos Part Name Code Table<a/>.
- Researched 83 taxon names not in Arctos
 
### Bioscience
#### Teresa
##### Benefits all Arctos Collections
 - Added 62 higher geography for mollusk collection
 - Created barcodes for all rooms, cabinets, drawers, shelves, and insect traps in Biosci
 - Corrected relationship for MSB mammal records
 - Changed barcodes on NMMNH:Mamm specimens at MSB
 
##### Benefits NMMNH Bioscience
 - Assisted Lindsey with Herbarium Bulkload questions
 - Trained Paula on pulling information from specimens cataloged in other collections with which we share a specimen
 - Instructed Paula on entering UTM and TRS data
 - Assisted with locality for bird specimen shared with MSB
 - Completed "Manage Collection" for all collections adding museum logo to record header and details for future publication to aggregators.
 - Downloaded 5,798 records shared with MSB and prepped bulkload file for load to NMMNH:Mamm collection.
 - Corrected relationship for MSB mammal records
 - Claimed barcodes for all collections: NMMNH followed by up to 12 numeric or text characters plus _ or -
 
#### Lindsey
##### Benefits NMMNH Bioscience
 - Bulkloaded 3638 Herbarium specimen records
 - Marked Paulas 98 mollusc records to load, loaded
 - Approved and marked Paulas 521 Bird records to load, loaded many of them but some have errors. Lindsey Fixed
 - Ordered, received and inventoried 98% of digtization eqiupment
 - Bulkloaded ~7300 arthropod records
 - Researched alcohol arthropod digitzation techniques
 - Maintaining a running budget for the Grant
   - estimating costs for budget exention until end of September
 - Bulk uploaded ~6000 mammal records that Teresa downloaded from MSB
 - Fixed 488 invertebrate agents
 - Fixed mollusc taxonomy to be able to upload into Arctos
 - Created and launched 3 NM Backyard iNaturalist challenges
   - NM Backyard Biodiversity Challenge https://www.inaturalist.org/projects/nm-backyard-biodiversity-challenge?tab=stats
   - NM Backyard Angiosperm Biodiversity https://www.inaturalist.org/projects/nm-backyard-angiosperm-biodiversity?tab=stats
   - NM Backyard Bird Biodiversity https://www.inaturalist.org/projects/nm-backyard-bird-biodiversity?tab=stats
 - Hosting weekly Digitization meetings
 - Bulkloaded ~15400 Invertebrate/mollusc records
 - Bulkloaded ~15400 Invertebrate/mollusc parts
 - Fixed 200 unicode specific locality problems
 - Bulkloaded ~419 non-tissued mammals
 - Supported, edited and tweeted 28 Bioscience tweets since November 2019 to the end of May 2020
 - Worked with Andrea and other social media temp staff to get 4 posts onto the main Facebook page during March/April/May 2020
 

#### Paula
##### Benefits NMMNH Bioscience
 - Entered 520 bird records through the Data Entry Screen in Arctos
 - Bulkloaded 98 mollusc records
 - Edited bird issues - locality and dates
 - Photographed 4 bird specimens for loan to SMNHC
 - Photographed 2 insect specimens with temporary and current labels for potential format change
 - Photographed 8 Birds for report
 - Photographed 12 skulls and shells in light box.
 - Photographed several different kinds of plant for contrast between light stand and light box image quality
 - Trained Hannah in basic photography workflow
 - Developed tentative protocals for imaging insects and birds/mammals and mollusks
 - Developed tentative protocols for imaging herbarium
 - Developed tentative protocols for imaging wet collection
 - Developed tentative protocols for imaging arthropods -Trouble shooting Lightbox work flow.
 - Digitization material research and testing
 - Photographing presentation specimens for mammals and molluscs.
 - Outline Photography Procedure manual
 - Decide on format for procedures final project
 - Developed 2nd Grant ideas
 - Weekly photographs of AWTNM
 - 4 Social Media posts
 - Compiling a list of images for PPM
 - Weekly documentation of "A Walk Through New Mexico" exhibit for digital curation


