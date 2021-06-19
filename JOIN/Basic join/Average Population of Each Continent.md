

<img width="241" alt="11" src="https://user-images.githubusercontent.com/78076248/115147806-1e8ea680-a05d-11eb-9bc6-79cd80b25881.PNG">

< Solution 1 >

SELECT o.CONTINENT, FLOOR(AVG(i.POPULATION)) FROM CITY AS i JOIN COUNTRY AS o ON i.COUNTRYCODE=o.CODE GROUP BY o.CONTINENT;

< Solution 2 >

SELECT c1.continent, FLOOR(avg(c2.population))
FROM COUNTRY as c1
join city as c2 on c1.code = c2.countrycode
group by c1.continent

Function used here
-


Group by
- Gather data with given variables

Floor
- Round the number to the floor

AVG
- Get the average value
