# ETL_Projetc

Things that happen yearly and are not related between them - oscar awards, super bowl and gold price.

CSV files from Kaggle

1) Create SQL dbs
create table gold(
Year text,
Price float
);

create table oscar(
Year text,
category text,
winner text,
film text
);

create table sb(
Year text,
SB text,
Attendance int,
QB_Winner text,
Coach_Winner text,
sb_Winner text,
Winning_Pts int,
QB_Loser text,
Coach_Loser text,
sb_Loser text,
Losing_Pts int,
MVP text,
Stadium text,
City text,
State text,
Point_Difference int
);


2) pandas/python in jupyter:load, read and print files to review structure
3) reviw dtypes and be sure dates are homogenieus between all df
4) mantain only actor category for oscar
5) the three files are modified to show info from 1967 (first super bowl) to 2018.
- Erase from gold first years until '67 (first 17 factors with iloc)
- Erase from oscar last years - 2018 and further (eliminate all with 19 or 20 in "Year" column)
6) Homogeniaze date as year in a "AA" format and trasform, if needed, dates into string
7) create a new file with all the information I want (the one in SQL db)
8) Connect to local database using psycopg2-binary to SQL PgAdmin & check tables
9) Append data frame into local database
10) join with natural 3 tables
11) save as a new table
12) save as CSV