# MS Access to Arctos Mapping

## LOCALITY Fields

LOCALITY field | function | Arctos "research" Locality BULKLOAD Field
--- | --- | ---
locality|CONCATENATE("NMMNH:Paleo:L-",**locality**) |LOCALITY_NICKNAME
datefound| |GEO_ATT_VALUE_1
origloc| |GEO_ATT_VALUE_4
fieldno| |GEO_ATT_VALUE_5
locale|IF(ISBLANK(**locale**),IF(ISBLANK(**topodata**),"no specific locality recorded",**topodata**),IF(ISBLANK(**topodata**),**locale**,CONCATENATE(**locale**,", ",**topodata**)))|SPEC_LOCALITY
collno
ffname
fmidinit
flname
tnsp
rnge
sec
coordinate
state
statelong
county
country
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
