# hackerrankrdbms

<h1>  SQL HACKER RANK </h1>
<table>
<tr>
<b> BASIC QUERY</b> <br> <br>
</tr>
<tr>
•	Revising the Select Query : Query all columns for all American cities in CITY with populations larger than 100000. The CountryCode for America is USA. 
   <br> 
   <b> QUERY:  SELECT * FROM CITY WHERE POPULATION >= 100000 and COUNTRYCODE LIKE '%USA' </b>  <br>
  <br> 
</tr>
<tr>
•	Revising the Select Query II: Query the names of all American cities in CITY with populations larger than 120000. The CountryCode for America is USA <br> 
 <b> QUERY: SELECT DISTINCT NAME FROM CITY WHERE POPULATION > 120000 and COUNTRYCODE LIKE '%USA' </b>   <br>
 <br>
</tr>
<tr>
•	Select All : Query all columns (attributes) for every row in the CITY table.  <br>
<b> QUERY: SELECT * FROM CITY </b>  <br> 
<br>
</tr>
<tr>
•	Select By ID : Query all columns for a city in CITY with the ID 1661.  <br>
<b>QUERY:SELECT * FROM CITY WHERE ID=1661 </b>  <br>
<br>
</tr>
<tr>
• Japanese Cities' Attributes QUERY: Query all attributes of every Japanese city in the CITY table. The COUNTRYCODE for Japan is JPN.  <br>
<b> SELECT * FROM CITY WHERE COUNTRYCODE LIKE'%JPN'  </b> <br>
<br>
</tr>
<tr>
• Japanese Cities' Names : Query the names of all the Japanese cities in the CITY table. The COUNTRYCODE for Japan is JPN. <br>
<b> SELECT NAME FROM CITY WHERE COUNTRYCODE='JPN'  </b> <br>
<br>
</tr>
<tr>
• Weather Observation Station 1: Query a list of CITY and STATE from the STATION table <br>
<b> SELECT CITY,STATE FROM STATION  </b> <br>
<br>
</tr> 
<tr>
• Weather Observation Station 3: Query a list of CITY names from STATION with even ID numbers only. You may print the results in any order, but must exclude duplicates from your answer.  <br>
<b> SELECT DISTINCT CITY FROM STATION  WHERE ID % 2 = 0  </b> <br>
<br>
</tr> 
<tr>
• Weather Observation Station 4: Let  be the number of CITY entries in STATION, and let  be the number of distinct CITY names in STATION; query the value of  from STATION. In other words, find the difference between the total number of CITY entries in the table and the number of distinct CITY entries in the table.   <br>
<b> SELECT COUNT(CITY) - COUNT(DISTINCT CITY) FROM STATION  </b> <br>
<br>
</tr> 
<tr>
• Weather Observation Station 5: Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.  <br>
<b>  (SELECT CITY, LENGTH(CITY) AS l FROM STATION ORDER BY l DESC LIMIT 1) UNION (SELECT CITY, LENGTH(CITY) AS l FROM STATION ORDER BY l ASC LIMIT 1);  </b> <br>
<br>
</tr> 
<tr>
• Weather Observation Station 6: Query the list of CITY names starting with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.  <br>
<b>  SELECT CITY FROM STATION WHERE CITY REGEXP '^a|^e|^i|^o|^u'  </b> <br>
<br>
</tr> 
<tr>
• Weather Observation Station 7: Query the list of CITY names starting with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.  <br>
<b>  SELECT DISTINCT CITY 
FROM   STATION 
WHERE  UPPER(CITY) LIKE '%A' 
   OR  UPPER(CITY) LIKE '%E' 
   OR  UPPER(CITY) LIKE '%I' 
   OR  UPPER(CITY) LIKE '%O' 
   OR  UPPER(CITY) LIKE '%U';  </b> <br>
<br>
</tr> 
<tr>
• Weather Observation Station 8: Query the list of CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates.  <br>
<b> SELECT DISTINCT city
FROM   station
WHERE  city RLIKE '^[aeiouAEIOU].*[aeiouAEIOU]$'  </b> <br>
<br>
</tr> 
<tr>
• Weather Observation Station 9: Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates. <br>
<b> SELECT DISTINCT city
FROM   station
WHERE  city RLIKE '^[^aeiouAEIOU].*'  </b> <br>
<br>
</tr> 
<tr>
• Weather Observation Station 10: Query the list of CITY names from STATION that do not end with vowels. Your result cannot contain duplicates. <br>
<b> SELECT DISTINCT city FROM station WHERE city RLIKE '.*[^aeiouAEIOU]$'  </b> <br>
<br>
</tr> 
<tr>
• Weather Observation Station 11:Query the list of CITY names from STATION that do not start with vowels and do not end with vowels. Your result cannot contain duplicates.  <br>
<b> SELECT DISTINCT city
FROM   station
WHERE  city RLIKE '^[^aeiouAEIOU].*[^aeiouAEIOU]$'  </b> <br>
<br>
</tr> 
<tr>
•  Higher Than 75 Marks : Query the Name of any student in STUDENTS who scored higher than  Marks. Order your output by the last three characters of each name. If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID.  <br>
<b> SELECT DISTINCT city
 SELECT DISTINCT NAME FROM  STUDENTS  WHERE MARKS > 75 ORDER BY RIGHT(NAME,3),ID; </b> <br>
<br>
</tr> 
<tr>
•  Employee Names :Write a query that prints a list of employee names (i.e.: the name attribute) from the Employee table in alphabetical order.   <br>
<b> SELECT NAME FROM Employee ORDER BY NAME </b> <br>
<br>
</tr> 
<tr>
•  Write a query that prints a list of employee names (i.e.: the name attribute) for employees in Employee having a salary greater than  per month who have been employees for less than  months. Sort your result by ascending employee_id.   <br>
<b> SELECT NAME FROM EMPLOYEE WHERE SALARY > 2000 AND MONTHS 10 </b> <br>
<br>
</tr> 
</table>
<h1>  Basic Join Challenges </h1>
<table>
<tr>
•  Given the CITY and COUNTRY tables, query the sum of the populations of all cities where the CONTINENT is 'Asia'.
Note: CITY.CountryCode and COUNTRY.Code are matching key columns.   <br>
<b> SELECT SUM(CITY.POPULATION) FROM CITY,COUNTRY WHERE  COUNTRYCODE = CODE  AND CONTINENT = "Asia" </b> <br>
<br>
</tr> 
<table>
<tr>
•  Given the CITY and COUNTRY tables, query the names of all cities where the CONTINENT is 'Africa'. Note: CITY.CountryCode and COUNTRY.Code are matching key columns.  <br>
<b> SELECT DISTINCT  CITY.NAME FROM  CITY,COUNTRY  WHERE CITY.CountryCode = COUNTRY.Code  AND COUNTRY.CONTINENT="Africa" </b> <br>
<br>
</tr> 
<tr>
•  Given the CITY and COUNTRY tables, query the names of all the continents (COUNTRY.Continent) and their respective average city populations (CITY.Population) rounded down to the nearest integer.   <br>
<b> SELECT Country.Continent, FLOOR(AVG(City.Population))
FROM Country, City 
WHERE Country.Code = City.CountryCode 
GROUP BY Country.Continent ; </b> <br>
<br>
</tr> 
