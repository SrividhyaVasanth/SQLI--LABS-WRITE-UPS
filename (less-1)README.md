to solve sqli-level-1 we first go to the main page
<img width="910" alt="sqli1" src="https://user-images.githubusercontent.com/76178081/104835653-1001e900-58ce-11eb-95f4-bfa2c393891a.PNG">

This challenge is based on SQL ERROR BASED INJECTIONS
This happens when an we try to create an address in the database and we use that error to mainpulate or extract data according to our requirements
commonly used injections like ' OR '1'='1-- (-- used to comment out everything)
so, for example an sql statement would look like

SELECT * FROM <TABLENAME> WHERE ' OR '1'='1--


We use fuzzing where we change the 'id'tag to 1,2 or 3
FUZZING can be described when we want send a lot of requests by entering different data( in this case \?id=3 . \?id=4  and \?id=9 gives us the same 
output i.e username and password) and these requests will trigger the application.


<img width="958" alt="sqli2" src="https://user-images.githubusercontent.com/76178081/104836586-e1d3d780-58d4-11eb-8883-a2e9e0d62c8f.PNG">

Another thing to be noticed is that when we enter a string it does give us the desired output and does not trigger the application
over here we give the string as ?id=okay and it does not give the corresponding username and password


<img width="922" alt="sqli3" src="https://user-images.githubusercontent.com/76178081/104837040-11d0aa00-58d8-11eb-8874-f28a76cbe55c.PNG">

