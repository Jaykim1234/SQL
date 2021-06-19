https://www.hackerrank.com/challenges/the-report/problem

<img width="259" alt="1" src="https://user-images.githubusercontent.com/78076248/115391155-6f2e0d00-a1df-11eb-9969-e8fea550df3c.PNG">

<img width="257" alt="2" src="https://user-images.githubusercontent.com/78076248/115391165-71906700-a1df-11eb-9013-36bf93713153.PNG">

< Solution 1 >

select if(g.grade<8,NULL,s.name),
g.grade,  s.marks
FROM STUDENTs AS s
JOIN GRADES AS g
on s.marks between g.Min_Mark and g.Max_Mark
order by g.grade desc, s.name, s.marks
;

< Solution 2 >

select 
case s1.name when g1.grade < 8 then s1.name else NULL end ,
g1.grade, s1.marks 
from students as s1
join grades as g1 on
s1.marks between g1.min_mark and g1.max_mark
order by g1.grade desc, s1.name;

## Function

# 조건 if문
if(조건, 조건 충족시, 조건 미달시)

# join 조건문
join ~ on 변수 between 범위1 and 범위 2

# order
order by 변수1 decs, 변수2,변수3
변수 1은 decs이지만 변수 2와 변수 3은 asec
