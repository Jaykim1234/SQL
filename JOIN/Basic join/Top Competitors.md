<img width="281" alt="1" src="https://user-images.githubusercontent.com/78076248/115998528-f3b9ca80-a5e7-11eb-8f3f-2caa86650ed2.PNG">
<img width="217" alt="2" src="https://user-images.githubusercontent.com/78076248/115998529-f5838e00-a5e7-11eb-8e3e-601507bb208b.PNG">
<img width="365" alt="3" src="https://user-images.githubusercontent.com/78076248/115998534-f74d5180-a5e7-11eb-9260-adafd6d899d2.PNG">
<img width="335" alt="4" src="https://user-images.githubusercontent.com/78076248/115998540-fa484200-a5e7-11eb-86b8-d526b7e6f55b.PNG">

select h.hacker_id, h.name from submissions as s 
join Challenges as c on s.challenge_id  = c.challenge_id  
join Difficulty as d on d.difficulty_level = c.difficulty_level 
join hackers as h on h.hacker_id = s.hacker_id
where d.score = s.score
group by h.hacker_id, h.name
having count(*)>1
order by count(*) desc, h.hacker_id


- Code
# select ㅁ.variable ~~~ group by ㅁ.variable
select하는 변수들 Group by로 하는 변수랑 일치시켜야 한다.

# count(*)
전체를 세는 것

# order by 
desc 안쓰면 asec으로 된다.
