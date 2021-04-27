Link:https://www.hackerrank.com/challenges/harry-potter-and-wands/problem


![image](https://user-images.githubusercontent.com/78076248/116225296-f59f9d00-a751-11eb-8fec-2e5eccff7543.png)
![image](https://user-images.githubusercontent.com/78076248/116225350-0223f580-a752-11eb-8410-d08386c9556a.png)

Previous trial

select id, age, m.coins_needed, m.power from (select code, power, min(coins_needed) as coins_needed from wands group by code, power) as m join wands as w on w.code=m.code and w.power =m.power and w.coins_needed = m.coins_needed join property as p on m.code = p.code where p.is_evil = 0 order by power desc, age desc

My solution
![image](https://user-images.githubusercontent.com/78076248/116225175-cc7f0c80-a751-11eb-8ada-3292a40b65c4.png)


## Function

# 괄호를 해서 전체 지정 가능
(select ~ ) as m

# and
join on ~ and ~ and 해서 조건 추가 가능

# join 두 번 
처음에 괄호로 묶은거에다가 join으로 또 묶는거 가능 
여기서 where 쓰고 natural join처럼 조건에 맞는거만 또 뽑는게 가능한거 같다.
