![image](https://user-images.githubusercontent.com/78076248/117680280-4d59f180-b1b1-11eb-827e-a3734c17a303.png)
![image](https://user-images.githubusercontent.com/78076248/117680322-58148680-b1b1-11eb-81e3-131973b6ea45.png)

select  s.name from Students as s
join Friends as f on s.id = f.id  
join Packages as p on s.id = p.id
join

(select f.id, p.salary from friends as f 
join packages as p on f.friend_id = p.id) as m on s.id = m.id

where p.salary < m.salary
order by m.salary 
