REFERENCES- https://gbhackers.com/perform-manual-sql-injection/



The payload used is ?id=1 and 1=1--+ 


<img width="954" alt="sqli9" src="https://user-images.githubusercontent.com/76178081/104888773-38075000-5993-11eb-8340-73fd66e319cd.PNG">

SQL QUERY for this would be

SELECT * FROM Dhakkan WHERE Your Login name=Dumb AND Your Password=' --+';
