to solve sqli-level-1 we first go to the main page
<img width="910" alt="sqli1" src="https://user-images.githubusercontent.com/76178081/104835653-1001e900-58ce-11eb-95f4-bfa2c393891a.PNG">

This challenge is based on SQL ERROR BASED INJECTIONS
This happens when an we try to create an address in the database and we use that error to mainpulate or extract data according to our requirements
commonly used injections like ' OR '1'='1-- (-- used to comment out everything)
so, for example an sql statement would look like

SELECT * FROM <TABLENAME> WHERE ' OR '1'='1' -- 
  
My intial first approach was to use normal sql injections such as OR '1'='1' --'  ór even OR '1'='1' /* 
When i used OR '1'='1' /*  as in http://localhost:8888/sqli-labs-php7-master/sqli-labs-php7-master/Less-1/?OR%20%271%27=%271%27%20/*

This how the query would look like

SELECT username,password WHERE '?id'=0 OR 1=1;

'1=1'is universally a true statement
 I get URL not found hence,  we cannot use this option
 
Another way to create an error in the application is to use limit 0,1 to extract data from a database
We get an error in the sql syntax
http://localhost:8888/sqli-labs-php7-master/sqli-labs-php7-master/Less-1/?id=%270%27%27|%20limit%200,1








<img width="958" alt="sqli2" src="https://user-images.githubusercontent.com/76178081/104836586-e1d3d780-58d4-11eb-8883-a2e9e0d62c8f.PNG">
we get username and password
SQL query will look like

SELECT  username,password from 'users' WHERE ?id=9

(We need to note that replace 9 with 0 or a two digit or a three digit number we will not get the same desired result as in the case of ?id=9}




Another thing to be noticed is that when we enter a string it does give us the desired output and does not trigger the application
over here we give the string as ?id=okay and it does not give the corresponding username and password



<img width="922" alt="sqli3" src="https://user-images.githubusercontent.com/76178081/104837040-11d0aa00-58d8-11eb-8874-f28a76cbe55c.PNG">

