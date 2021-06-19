<img width="308" alt="123" src="https://user-images.githubusercontent.com/78076248/115145865-2138ce00-a054-11eb-921d-4900ee0b773e.PNG">

Answer

< Solution 1 >

SELECT city.name 
FROM CITY  
JOIN COUNTRY on CITY.CountryCode = COUNTRY.Code 
where COUNTRY.CONTINENT = 'Africa'

< Solution 2 >

select c1.name 
from CITY AS c1, COUNTRY AS c2
where c1.countrycode = c2.code and
    c2.CONTINENT = 'Africa';


