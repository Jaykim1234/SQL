first trial
select m.hacker_id, h.name, m.cnt from 
(select  hacker_id, count(challenge_id) as cnt from challenges as c
group by hacker_id) as m
join Hackers as h 
on h.hacker_id = m.hacker_id
having cnt = (select count(challenge_id) from challenges as c1 group by c1.hacker_id order by count(*) desc Limit 1)
or cnt not in  (select count(challenge_id) from challenges as c2 group by c2.hacker_id having c2.hacker_id <> c.hacker_id)
order by cnt desc, h.hacker_id


#ONLINE ANSWERS

SELECT c.hacker_id, h.name, COUNT(c.challenge_id) AS cnt 
FROM Hackers AS h JOIN Challenges AS c ON h.hacker_id = c.hacker_id
GROUP BY c.hacker_id, h.name HAVING
cnt = (SELECT COUNT(c1.challenge_id) FROM Challenges AS c1 GROUP BY c1.hacker_id ORDER BY COUNT(*) DESC LIMIT 1) OR
cnt NOT IN (SELECT COUNT(c2.challenge_id) FROM Challenges AS c2 GROUP BY c2.hacker_id HAVING c2.hacker_id <> c.hacker_id);
