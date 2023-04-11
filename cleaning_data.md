
Data cleaning, or data cleansing, is the process of preparing raw data sets for analysis by handling data quality issues. 
The purpose:
    To ensure the data is valid and accurate, it's essential to clean it before analysis. 

    To help to obtain reliable information or predictions. 

    To help to obtain valuable insights for decision-making when Working with product, service, or system.

Data cleaning is important for the following reasons:
A- Makes the data set understandable
        Raw data may contain human, machine, or instrument issues, especially if obtained from multiple sources. By cleaning it, you can better understand data trends and patterns. 

B- Ensures data uniformity
        While using accurate data records is essential, checking they're consistent throughout the data set is also crucial. 

C- Retains only relevant information
        Raw data may also contain records that may not be valuable for predictions or analysis. Handling these records through data cleansing can help ensure information quality. 

To obtain cleaned data records we have to follow:
1. Establish data set cleaning objectives
2. Create a structure to follow
3. Identify duplicate data records
4. Handle outliers
5. Resolve missing data records


Queries:
Below, provide the SQL queries you used to clean your data.

I'll write some samples from the query codes

Let take the all_sessions table

1- Missing value(NULL)

to test and search about the NULL or missing data, I wrote varity different codes

SELECT ecommerceaCtion_option 
FROM all_sessions
WHERE ecommerceaCtion_option IS NULL

SELECT DISTINCT searchkeyword 
FROM all_sessions
GROUP BY searchkeyword
WHERE searchkeyword IS NULL

SELECT DISTINCT pagetitle 
FROM all_sessions
GROUP BY pagetitle
HAVING pagetitle>1;

SELECT DISTINCT itemrevenue, COUNT(*)
FROM all_sessions
GROUP BY itemrevenue


If I found the column, completely NULL or the percentage of data less than 50%. Thus I drop it

    Columns that dropped:
    1- userid
    2- ecommerceaCtion_option
    3- searchkeyword
    4- transactionrevenue
    5- itemrevenue
    6- itemquantity
    7- productrevenue
    8- productquantity
    9- productrefundamount
    10- transactions



-- COLUMN DROP
ALTER TABLE all_sessions
DROP COLUMN ecommerceaCtion_option

If I found the column contains some Null data, I examine the type of Data to fill the missing attributes, by calculating the average or write a word

UPDATE all_sessions
SET pagetitle = 'Other'
WHERE pagetitle IS NULL

UPDATE all_sessions
SET timeonsite = 224
WHERE timeonsite IS NULL

2- Removing Duplicate rows

SELECT DISTINCT productsku, visitid, fullvisitorid, COUNT(*) 
FROM all_sessions
GROUP BY productsku, visitid, fullvisitorid
HAVING(COUNT(*)>1);

SELECT *
, ROW_NUMBER() OVER (PARTITION BY productsku, visitid) as rn
FROM all_sessions


SELECT * FROM(
	SELECT*
	, ROW_NUMBER() OVER (PARTITION BY productsku, visitid) as rn
	FROM all_sessions) x
WHERE x.rn>1;	

DELETE FROM all_sessions
WHERE productsku in (
					SELECT productsku
					FROM(
						SELECT*
						, ROW_NUMBER() OVER (PARTITION BY productsku, visitid) as rn
						FROM all_sessions) x
					WHERE x.rn>1);


3- Check the Datatype and create the tables according to the type of data.

4- Check the structural errors. I do not notice any error "typo"

5- Convert the format. For the large numbers in some tables, I define it's format when creating the tables "FLOAT". The date format is good and perfect to calculate the revenue monthely ,daily or yearly. 



