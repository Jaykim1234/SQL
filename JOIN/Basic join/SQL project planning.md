![image](https://user-images.githubusercontent.com/78076248/117099630-f2b83400-ad71-11eb-80d2-ba0a3e5fb813.png)
![image](https://user-images.githubusercontent.com/78076248/117099652-fd72c900-ad71-11eb-81af-b7172ade380f.png)



select Start_Date, min(end_date) from 

(select Start_Date from Projects
where Start_Date not in (select end_Date from Projects)) as t1, 

(select end_Date from Projects
where end_Date not in (select start_Date from projects)) as t2

where start_DATE < END_DATE
group by start_date
order by datediff(min(end_date), start_date), start_date;

## Function

# from 다음에 두  개 써도 된다. (t1, t2)

# where 다음에 조건 사용 가능

# datediff( 왼쪽, 오른쪽) = 왼쪽 - 오른쪽
