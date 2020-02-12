# Data-Protocols
## Annual Database
The [Kluane Red Squirrel Project](www.redsquirrel.ca) is a long-term study of individually marked North American red squirrels in the southwestern Yukon Territory of Canada.  All data are collected in the field according to standardized field protocols.  Data are entered in the field into iPod Touch devices with a custom app.  This app syncs with our field database once the field workers return to camp.  The field database is a MySQL database with a custom front end written in Java using a program called Grails.  The field database is housed on a laptop that is used as a server, which allows multiple data entry laptops to communicate with the database through a local wifi network in camp.  The field database is backed up daily and weekly dumps are emailed to McAdam.

## Meta-Data and Coding
Meta-data and coding for the database are described in the files within this folder.

## Long-Term Database
At the end of the field season, the annual database is merged with the long-term database.  At this time any errors that have been identified in the long-term database are corrected.  All errors that are discovered in the database should be logged [here](https://github.com/KluaneRedSquirrelProject/KRSP-Database-Errors/issues).  All corrected errors in the long-term database are corrected through a query.  These ErrorFix queries are also included [here](https://github.com/KluaneRedSquirrelProject/KRSP-Database-Errors).  In addition, annual archives of the long-term database are made.  As a result, all previous versions of the database can be recreated.  Once the database is cleaned, a version of the database is archived and a new annual field database is launched.  Once the field database is active, no further changes are made to the long-term database to prevent conflicts.

## Accessing the Long-Term Database
The long-term database is stored in the cloud and can be accessed directly from the cloud using R and RStudio and a custom R package called [krsp](https://github.com/KluaneRedSquirrelProject/krsp).  Accessing the database in the cloud requires login credentials.  Contact McAdam if you do not have login credentials yet.  

## Manipulating and Analyzing Data
All manipulation of data and analyzing of data should be done using reproducible code that pulls direclty from the cloud instance of the database.  Users of the database should NOT download the database and work from local instances.  [R code and functions](https://github.com/KluaneRedSquirrelProject/krsp-functions) have been written to perform common tasks.  The use of this common code maintains consistency and allows users to perform tasks and answer questions faster.
