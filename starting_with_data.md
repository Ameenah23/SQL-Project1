Question 1: 

SQL Queries:
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
          
[allsessions-data-1681186561449.csv](https://github.com/Ameenah23/SQL-Project1/files/11196505/allsessions-data-1681186561449.csv)


Answer: 
Some of columns that contain duplicate records
productsku
visitid
fullvisitorid




Question 2: 

SQL Queries:
SELECT COUNT(fullvisitorid) 
FROM all_sessions

Answer:

total number of unique visitors (`fullVisitorID`)= 14873

Question 3: 

SQL Queries:
SELECT COUNT(visitid) 
FROM all_sessions

Answer:

total number of unique visitors (`visitid`)= 14873

Question 4: 

SQL Queries:

SELECT visitid, total_ordered, COUNT(*)
FROM all_sessions aa
JOIN sale_report bb
	ON aa.productsku=bb.productsku 
GROUP BY visitid, total_ordered
HAVING visitid > 1
LIMIT 10;

Answer:
visitid	total_ordered	count
1496949281	1	1
1470268175	43	1
1472109793	11	1
1496567631	30	1
1470868446	3	1
1481730283	50	1
1494337059	2	1
1474204584	9	1
1489308957	85	1
1487804892	50	1

[Starting-Q4-data-1681186452321.csv](https://github.com/Ameenah23/SQL-Project1/files/11196493/Starting-Q4-data-1681186452321.csv)


Question 5: 

SQL Queries:

WITH t1 AS 
 (SELECT visitid, productprice, Count(*) AS n 
  FROM all_sessions
  GROUP BY visitid, productprice)
SELECT visitid, productprice, n, 
       (0.0+n)/(COUNT(*) OVER (PARTITION BY visitid)) as percentage-- no integer divide!
FROM t1;

Answer:

[Starting Q5-data-1681180894471.csv](https://github.com/Ameenah23/SQL-Project1/files/11196442/Starting.Q5-data-1681180894471.csv)

