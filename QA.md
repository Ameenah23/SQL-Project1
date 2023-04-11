What are your risk areas? Identify and describe them.

There are many risks factors that affect usually on any project, like;
    - Increased costs and more time spent on developing  products. ...
    - Increased risk of security breaches. ...
    - Unstable performance and undetected errors. ...
    - lack of consistent results.
    - The cost of a test. 
    - Analytical turnaround time. ...
    - The quality and reliability of data and test results.

For me 
I think the critical risk when decide to remove the rows and data. I ask myself if this step is write and not affect on the results and the decision. If choose the best codes that describe the data or not , if make any mistakes. 
https://medium.com/learning-sql/sql-quality-assurance-queries-9727df6bed5b

But
By following the directions, steps of cleaning data and the courses online, on compass and on youtube how to build the codes. I tried to decrease the risk of QA processes.

By checking the accuracy and quality of data for every step.

By checking 
    - complete (i.e. no blank or null values)
    - unique (i.e. no duplicate values)
    - consistent with what we expect (eg. a decimal between a certain range)

I think the critical risk when decide to remove the rows and data. I ask myself if this step is write and not affect on the results and the decision. If choose the best codes that describe the data or not , if make any mistakes.  


QA Process:
Describe your QA process and include the SQL queries used to execute it.

1- Start reading the requirments. then reading the matterial course on campass and lectures.
2- Figure out what I need before performing the project. What are the strongest and weakest points about my situation.
3- I found I need to review different matterials to be familiar with SQL. I watch many lectures online and practices. Then watching on youtube many videos how to make data cleaning and how to choose the best code to make the removing deplicate.
4-Download the files.csv and check the data to know what is the best format to create the tables.
5- Cleaning data and check statistical rules like average , max, min ..ect
6- Counting the percentage to decide if deleting and removing the data or not ...ect.

I tested many codes to find what is the best code should be chosen . EXample, to remove the duplicate in case multi column or rows, I wrote a code, it was perfect and applied on the reading data to find the matches. When I sent the job to perform through the port, it takes more than 40 minutes and not finish.
Thus I decided to write another code that faster to perform the analyzing the data. If I wait to get a result, I would not be able to finish from the project on time.

Removing Duplicate rows

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

========
SELECT aa.country, aa.city, SUM(ck.total_ordered * aa.productprice) as total
	, ROW_NUMBER() OVER (PARTITION BY aa.country ORDER BY SUM(ck.total_ordered * aa.productprice)) as seqnum
      FROM all_sessions aa
	  INNER JOIN sales_by_sku ck
           ON aa.productsku = ck.productsku
GROUP BY country, city
ORDER BY country;



