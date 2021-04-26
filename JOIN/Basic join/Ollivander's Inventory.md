/*
Enter your query here.
*/
select id, age, m.coins_needed, m.power from
(select code, power, min(coins_needed) as coins_needed from wands
group by code, power) as m
join wands as w on w.code=m.code and w.power =m.power and w.coins_needed = m.coins_needed
join property as p on m.code = p.code
where p.is_evil = 0
order by power desc, age desc

SELECT id, age, m.coins_needed, m.power FROM 
(SELECT code, power, MIN(coins_needed) AS coins_needed FROM Wands GROUP BY code, power) AS m
JOIN Wands AS w ON m.code = w.code AND m.power = w.power AND m.coins_needed = w.coins_needed
JOIN property AS p ON m.code = p.code
WHERE p.is_evil = 0
ORDER BY m.power DESC, age DESC;
