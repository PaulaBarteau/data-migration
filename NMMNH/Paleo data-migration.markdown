# MS Access to Arctos Mapping

## LOCALITY Fields

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


### function definitions

* locname
CONCATENATE("NMMNH:Paleo:L-",**locality**) 

* specloc
IF(ISBLANK(**locale**),IF(ISBLANK(**topodata**),"no specific locality recorded",**topodata**),IF(ISBLANK(**topodata**),**locale**,CONCATENATE(**locale**,", ",**topodata**))) 

* specverbatimloc  
IF(ISBLANK(**country**),IF(ISBLANK(**state**),"N/A",**state**),IF(ISBLANK(**state**),**country**,CONCATENATE(**country**,", ",**state**)))=vcountrystate then IF(ISNA(vcountrystate),IF(ISBLANK(**county**),"N/A",**county**),IF(ISBLANK(**county**),vcountrystate,CONCATENATE(vcountrystate,", ",**county**)))=vstatecounty then IF(ISNA(vstatecounty),IF(ISBLANK(**locale**),"N/A",E2),IF(ISBLANK(**locale**),vstatecounty,CONCATENATE(vstatecounty,", ",**locale**)))=vcountylocale then IF(ISNA(vcountylocale),IF(ISBLANK(**mapid**),"N/A",**mapid**),IF(ISBLANK(**mapid**),vcountylocale,CONCATENATE(vcountylocale,", ",**mapid**)))=vlocalemapid then IF(ISNA(vlocalemapid),IF(ISBLANK(**topodata**),"N/A",**topodata**),IF(ISBLANK(**topodata**),vlocalemapid,CONCATENATE(vlocalemapid,", ",**topodata**))) 

* section
IF(ISBLANK(**sec**),"N/A",CONCATENATE("sec",**sec**))
