:::EXPLANATION:::

The premade SQL database with the contents pre-uploaded can be gained using the "ActorBugDatabase.sql" file. Simply load it up into a database that is compatible with SQL formating to utilize it.

If a user decides to upload from the csv file itself, these are the ocmmands that were used for mysql to build the database originally. Modify them according to the syntax of the database being used.


:::BUILD THE DATABASE COMMNADS FOR MYSQL:::

create database Actor_Bugs_Database;

USE Actor_Bugs_Database;

CREATE TABLE ActorBugs(Bug_Name varchar(100) NOT NULL, Web_Link varchar(255) NOT NULL, Issue_Title varchar(255) NOT NULL, Actor_Characteristic varchar(25) NOT NULL, Actor_SubCategory varchar(25) NOT NULL, CBS_Aspect varchar(10) NOT NULL, CBS_Software varchar(10) NOT NULL, CBS_Implication varchar(10) NOT NULL, PRIMARY KEY (Bug_Name));

LOAD DATA LOCAL INFILE 'Actor_Bug_Database.csv' INTO TABLE ActorBugs COLUMNS TERMINATED BY '|' LINES TERMINATED BY '\n';



:::EXAMPLE QUERIES:::
SELECT Bug_Name, CBS_Aspect, CBS_Software, CBS_Implication FROM ActorBugs WHERE Bug_Name LIKE '%Squbs%';

SELECT Bug_Name, Actor_Characteristic, CBS_Aspect, CBS_Software, FROM ActorBugs WHERE Actor_Characteristic LIKE '%Logic%';

*NOTE* as the Web_Link and Issue_Title can be very long, depending on the interface used, such as a command line window, selecting multiple columns including those can cause presentation/formatting issues.


