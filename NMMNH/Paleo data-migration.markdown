# NMMNH Paleontology Data Migration from MS Access to Arctos

## Migration Procedures

Because the NMMNH Paleo Collection data contains a very specific set of localities, it was determined that migration would proceed by locality, starting with NMMNH:Paleo:L-1. For each locality, the following steps were followed.

### Prepare the Migration Data File
 1. OPen a new Excel Data Migration Template. The template can be found at N:>GeoScience>Arctos>SpecimenBulkloads>Data Migration Template.xls.  
 2. Enter the locality number in cell B3 of the Workbook Description tab of the Data Migration Template.  
 3. Save the Template to the following directory: N:>GeoScience>Arctos>SpecimenBulkloads. The filename should be "L-" and the number of the locality.  
 4. Copy all catalog records for the locality from the MS Access SPECIMEN table into the SPECIMEN tab of the Data Migration File.  
 5. In the SPECIMEN tab, replace all blank values in the column [cdate] with "no date".  
 6. Copy the [cdate] column to column A of the Coll Events tab. Highlight Column A and select Data>Remove Duplicates from the main Excel menu. Do not expand the selection. The results will be a list of unique collection date values. These will be the collecting events associated with this locality. Highlight column A and select Data>Sort from the Excel main nemu. At the pop-up, select "Continue with the current selection", "Sort", then "OK". At the Sort Warning pop-up select "Sort numbers and numbers stored as text separately", then "OK".  
 7. Copy the line for the locality from the to the LOCALITY tab of the locality bulkload file and paste it into line 2 of the Locality tab of the Data Migration File.  
   


## MS Access to Arctos Mapping

### LOCALITY Fields

LOCALITY field | function | Arctos "research" Locality BULKLOAD Field | function | Arctos "research" Collecting Event Bulkload Field
--- | --- | --- | --- | ---
locality|locname|LOCALITY_NICKNAME| | 
datefound| |GEO_ATT_VALUE_1| | 
origloc| |GEO_ATT_VALUE_4| | 
fieldno| |GEO_ATT_VALUE_5| | 
locale|specloc|SPEC_LOCALITY|specverbatimloc|VERBATIM_LOCALITY
collno| |GEO_ATT_VALUE_6| | 
ffname| | | | 
fmidinit| | | | 
flname| | | | 
tnsp| |GEO_ATT_VALUE_7| | 
rnge| |GEO_ATT_VALUE_8| | 
sec|section|GEO_ATT_VALUE_9| | 
coordinate| |GEO_ATT_VALUE_10| | 
state| | |specverbatimloc|VERBATIM_LOCALITY
statelong| | | |  
county| | |specverbatimloc|VERBATIM_LOCALITY
country| | |specverbatimloc|VERBATIM_LOCALITY
utmzone
utmn
utme
nad
gps?
lat_long
lat
long
mapid
landstat
statmap
era
period
epoch
age
lvb
faunalzone
group
formation
member
stratdata
lithology
topodata
geography
specimens
loctype
accno
markloc
markloc2
pubid
pubs?
remarks
entered
searchloc
permit


#### function definitions

* locname
CONCATENATE("NMMNH:Paleo:L-",**locality**) 

* specloc
IF(ISBLANK(**locale**),IF(ISBLANK(**topodata**),"no specific locality recorded",**topodata**),IF(ISBLANK(**topodata**),**locale**,CONCATENATE(**locale**,", ",**topodata**))) 

* specverbatimloc  
IF(ISBLANK(**country**),IF(ISBLANK(**state**),"N/A",**state**),IF(ISBLANK(**state**),**country**,CONCATENATE(**country**,", ",**state**)))=vcountrystate then IF(ISNA(vcountrystate),IF(ISBLANK(**county**),"N/A",**county**),IF(ISBLANK(**county**),vcountrystate,CONCATENATE(vcountrystate,", ",**county**)))=vstatecounty then IF(ISNA(vstatecounty),IF(ISBLANK(**locale**),"N/A",E2),IF(ISBLANK(**locale**),vstatecounty,CONCATENATE(vstatecounty,", ",**locale**)))=vcountylocale then IF(ISNA(vcountylocale),IF(ISBLANK(**mapid**),"N/A",**mapid**),IF(ISBLANK(**mapid**),vcountylocale,CONCATENATE(vcountylocale,", ",**mapid**)))=vlocalemapid then IF(ISNA(vlocalemapid),IF(ISBLANK(**topodata**),"N/A",**topodata**),IF(ISBLANK(**topodata**),vlocalemapid,CONCATENATE(vlocalemapid,", ",**topodata**))) 

* section
IF(ISBLANK(**sec**),"N/A",CONCATENATE("sec",**sec**))
