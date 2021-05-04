https://github.com/Jaykim1234/SQL/new/main/JOIN/Basic%20join
![image](https://user-images.githubusercontent.com/78076248/116982410-0cea0780-acc9-11eb-85ec-73039e7a557f.png)

select m.hacker_id, h.name, sum(m.score) as total_score from
(select hacker_id, challenge_id, max(score) as score from Submissions
group by hacker_id, challenge_id) as m
join hackers as h on m.hacker_id = h.hacker_id
group by m.hacker_id, h.name
having total_score > 0
order by total_score desc, m.hacker_id ;

## Fuctions

#sum

#max

#주의사항

join 할 때 변수들이 서로 맞아야 join이 되니 잘 신경쓰기!!
