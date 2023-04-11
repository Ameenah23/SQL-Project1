Answer the following questions and provide the SQL queries used to find the answer.

    P[Q1-COUNTRY- data-1681135522048.csv](https://github.com/Ameenah23/SQL-Project1/files/11196231/Q1-COUNTRY-.data-1681135522048.csv)
[Q1- CITY- data-1681135438836.csv](https://github.com/Ameenah23/SQL-Project1/files/11196232/Q1-.CITY-.data-1681135438836.csv)

**Question 1: Which cities and countries have the highest level of transaction revenues on the site?**


SQL Queries:

SELECT DISTINCT city, MAX(city), COUNT(city)
FROM all_sessions
GROUP BY city
ORDER BY COUNT(city) DESC

SELECT DISTINCT country, MAX(country), COUNT(country)
FROM all_sessions
GROUP BY country
ORDER BY COUNT(country) DESC

Answer:
The connection correlation between the transaction revenues column with city and country could not find directly because it is NULL column and it was drop by data cleaning processes.

But we can find the Maximum frequency for the city and country as indicate to the highest level of transaction revenues on the site

The city: I found the highest level of transaction revenues on the site with frequency = 
not available in demo dataset = 8187
The second highest city is Mountain View = 1142

Whereas the highest country is
United States = 8547
The second highest country is 
India = 708

Please look at attachment files.

[Q1- CITY- data-1681135438836.csv](https://github.com/Ameenah23/SQL-Project1/files/11196304/Q1-.CITY-.data-1681135438836.csv)
[Q1-COUNTRY- data-1681135522048.csv](https://github.com/Ameenah23/SQL-Project1/files/11196314/Q1-COUNTRY-.data-1681135522048.csv)


**Question 2: What is the average number of products ordered from visitors in each city and country?**


SQL Queries:

SELECT Country, AVG(total_ordered)
FROM all_sessions aa
JOIN sale_report bb
	ON aa.productsku=bb.productsku 
GROUP BY Country
HAVING COUNT(*) > 1
ORDER BY AVG(total_ordered) DESC;


SELECT city, AVG(total_ordered)
FROM all_sessions aa
JOIN sale_report bb
	ON aa.productsku=bb.productsku 
GROUP BY city
HAVING COUNT(*) > 1
ORDER BY AVG(total_ordered) DESC;

Answer:
Please look at attachment files.

[Q2-CITY- data-1681138253086.csv](https://github.com/Ameenah23/SQL-Project1/files/11196328/Q2-CITY-.data-1681138253086.csv)

[Q2-COUNTRY- data-1681138197703.csv](https://github.com/Ameenah23/SQL-Project1/files/11196345/Q2-COUNTRY-.data-1681138197703.csv)

**Question 3: Is there any pattern in the types (product categories) of products ordered from visitors in each city and country?**


SQL Queries:

SELECT country, v2productcategory, COUNT(*)
FROM all_sessions 
GROUP BY v2productcategory, country
HAVING COUNT(*) > 1
ORDER BY COUNT(*) DESC;



SELECT city, v2productcategory, COUNT(*)
FROM all_sessions 
GROUP BY v2productcategory, city
HAVING COUNT(*) > 1
ORDER BY COUNT(*) DESC;



Answer:
YES
There is a pattern in the types (product categories) of products ordered from visitors in each city and country.

Please look at attachment files.

[Q3- COUNTRY- data-1681139703668.csv](https://github.com/Ameenah23/SQL-Project1/files/11196351/Q3-.COUNTRY-.data-1681139703668.csv)

[Q3-CITY-data-1681139443769.csv](https://github.com/Ameenah23/SQL-Project1/files/11196353/Q3-CITY-data-1681139443769.csv)


**Question 4: What is the top-selling product from each city/country? Can we find any pattern worthy of noting in the products sold?**


SQL Queries:

SELECT Country, v2productname, COUNT(total_ordered)
FROM all_sessions aa
JOIN sale_report bb
	ON aa.productsku=bb.productsku 
GROUP BY Country, v2productname
HAVING COUNT(*) > 1
ORDER BY country, COUNT(total_ordered) DESC;

SELECT city, v2productname, COUNT(total_ordered)
FROM all_sessions aa
JOIN sale_report bb
	ON aa.productsku=bb.productsku 
GROUP BY city, v2productname
HAVING COUNT(*) > 1
ORDER BY city, COUNT(total_ordered) DESC;

Answer:

Please look at attachment files.


Can we find any pattern worthy of noting in the products sold?
No any pattern.

[Q4- City -data-1681185899048.csv](https://github.com/Ameenah23/SQL-Project1/files/11196381/Q4-.City.-data-1681185899048.csv)

[Q4- Country- data-1681185835219.csv](https://github.com/Ameenah23/SQL-Project1/files/11196384/Q4-.Country-.data-1681185835219.csv)

**Question 5: Can we summarize the impact of revenue generated from each city/country?**

SQL Queries:
SELECT aa.country, aa.city, SUM(ck.total_ordered * aa.productprice) as total
	, ROW_NUMBER() OVER (PARTITION BY aa.country ORDER BY SUM(ck.total_ordered * aa.productprice)) as seqnum
      FROM all_sessions aa
	  INNER JOIN sales_by_sku ck
           ON aa.productsku = ck.productsku
      GROUP BY country, city



Answer:

Please look at attachment files.


[Q5-data-1681151839461.csv](https://github.com/Ameenah23/SQL-Project1/files/11196411/Q5-data-1681151839461.csv)





