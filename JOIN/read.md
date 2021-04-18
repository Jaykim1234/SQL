# SQL


-	DISTINCT removes duplicates
-	WHERE restricts rows returned
-	Joins:
o	A JOIN B

![image](https://user-images.githubusercontent.com/78076248/115145578-8f7c9100-a052-11eb-8cf0-90a889ab92c6.png)
o	Cross Join:
-	Only puts tables side by side
-	Like SELECT * From A,B
-	SELECT * FROM A CROSS JOIN B




<img width="317" alt="2" src="https://user-images.githubusercontent.com/78076248/115145601-b044e680-a052-11eb-9c6a-6ea462b3eacc.PNG">

o	Natural Join
-	Retrieves rows where id matches
-	More meaningful
-	Like SELECT a.col1, acolna FROM A,B where A.col1=B.col1…
-	Select * FROM A INNER JOIN B USING (col1,col2..)



![image](https://user-images.githubusercontent.com/78076248/115145642-da96a400-a052-11eb-80ad-98356ea886bb.png)
![image](https://user-images.githubusercontent.com/78076248/115145659-f00bce00-a052-11eb-98f0-06f15f6567e7.png)
o	Inner Join
 
