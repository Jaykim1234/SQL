https://www.hackerrank.com/challenges/the-company/problem


select * from company as c1

left join Lead_manager   as l1   on c1.company_code = l1.company_code
left join Senior_manager as s1   on l1.lead_manager_code = s1.lead_manager_code
left join Manager        as m1   on s1.senior_manager_code = m1.senior_manager_code
left join Employee       as e1   on m1.manager_code = e1.manager_code


select * from company as c1

join Lead_manager   as l1   on c1.company_code = l1.company_code
join Senior_manager as s1   on l1.lead_manager_code = s1.lead_manager_code
join Manager        as m1   on s1.senior_manager_code = m1.senior_manager_code
join Employee       as e1   on m1.manager_code = e1.manager_code
