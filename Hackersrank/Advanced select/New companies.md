https://www.hackerrank.com/challenges/the-company/problem


![image](https://user-images.githubusercontent.com/78076248/131999974-a2ab8a5c-e205-4e5c-9ef6-c40979ce6aac.png)

![image](https://user-images.githubusercontent.com/78076248/132000019-9e9971ec-f240-4efa-b35e-02b223a044ff.png)

![image](https://user-images.githubusercontent.com/78076248/132000055-42bb8096-aa06-466f-802a-ceee670ef348.png)


select 

c1.company_code, 
c1.founder, 
count(distinct l1.lead_manager_code), 
count(distinct s1.senior_manager_code),  
count(distinct m1.manager_code), 
count(distinct e1.employee_code)

from company as c1

right join Lead_manager as l1 on c1.company_code = l1.company_code 

right join Senior_manager as s1 on l1.lead_manager_code = s1.lead_manager_code 

right join Manager as m1 on s1.senior_manager_code = m1.senior_manager_code 

right join Employee as e1 on m1.manager_code = e1.manager_code

group by c1.company_code, c1.founder
