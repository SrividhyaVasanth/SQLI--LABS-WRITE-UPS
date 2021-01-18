Firstly we need to trigger an error in the application

used: ?id=1'
      ?id=okay
      Both of these do not trigger an error 
      We can try with double quotes(as the task suggests)
      
   <img width="922" alt="horse" src="https://user-images.githubusercontent.com/76178081/104924337-49685080-59c3-11eb-99ff-35ed0663dbd9.PNG">
   
   
   We can notice that the error is in ") in the syntax. 
   This means that the input that we provide is also enclosed in (" ")

      
<img width="847" alt="opera" src="https://user-images.githubusercontent.com/76178081/104925670-2179ec80-59c5-11eb-9141-a98ffb46b9ac.PNG">

SELECT Login id, Password FROM Tablename WHERE id=("user-input that should be provided by us");

 USED: ?id=1") --+
      
      
(+ is used instead of space or adding space in the URL)
