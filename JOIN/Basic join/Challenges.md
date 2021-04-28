first trial
select m.hacker_id, h.name, m.cnt from 
(select  hacker_id, count(challenge_id) as cnt from challenges as c
group by hacker_id) as m
join Hackers as h 
on h.hacker_id = m.hacker_id
having cnt = (select count(challenge_id) from challenges as c1 group by c1.hacker_id order by count(*) desc Limit 1)
or cnt not in  (select count(challenge_id) from challenges as c2 group by c2.hacker_id having c2.hacker_id <> c.hacker_id)
order by cnt desc, h.hacker_id
