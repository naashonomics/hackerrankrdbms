# hackerrankrdbms
<table>
<tr>
SQL HACKER RANK <br>
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
<br>
<b> SELECT NAME FROM CITY WHERE COUNTRYCODE='JPN'  </b> <br>
<br>
</tr>
<tr>
• Weather Observation Station 1: Query a list of CITY and STATE from the STATION table <br>
<br>
<b> SELECT CITY,STATE FROM STATION  </b> <br>
<br>
</tr> 

