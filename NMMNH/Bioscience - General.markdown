Dates:
 - Unknown dates use 1800-01-01; the current date will be used as the end date
 - If there is a prep date, we use the prep date for the end date.
 - If a year is provided, we use year-01-01 to year-12-31
 - If a year and month are provided we use yyyy-mm-01 to the last day of that month
 - summer: June to end of August. ex: Summer 1992 is 1992-06-01	to 1992-08-31
 - spring: March to end of May. ex: Spring 1995 is 1995-03-01	to 1995-05-31
 - fall: September to end of November. ex: Fall 1989	is 1989-09-01	to 1989-11-30



Types of Dates:
 - Identification Date: does not require full date
 - Attribute Date: Does not require full date
 - Detr. Date: REQUIRED (in case of no date use the first of the month or year)
 - VerbatimDate: Literally the date that is written as is, and put No date recorded.
 - Begin and End date: Earliest we know it was collected and then the latest



Statistics:
Localities for Herb: for 1000 speciemsn, to create verbatim locality, higher geography, and edit specific locality it took about 8 minutes per record (total of 2 hours). This is not including editing coordinates, and does not including adding features to higher geography (like a specific locality of Sandia Mountains, are in Cibola National Forest but this will be added at a later date during georeference.


Excel functions:
=datevalue to convert text dates to numerical dates
=trim() to get rid of extra spaces at the beginning, middle or end
 =VLOOKUP(uniqueidentifier(catnum),highlightentiretable,whichcolumntoreadfrom,FALSE)
