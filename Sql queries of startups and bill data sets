CREATE DATABASE STARTUPS;
USE  STARTUPS;
-- 2. show tables
select * from startups;
-- 3. View entire startups table

-- 4. Order by Profit (by default orders in ascending)

select * from startups
order by profit;
-- 5. Order by MKT in descending order
select * from startups
order by mkt  desc;


-- 6. Order by STATE 
select state, rnd, admin
from startups
order by state;

-- 7. Order by State descending order
select state, rnd, admin
from startups
order by state desc;


-- 8. Order by STATE and PROFIT
select state, profit from startups
order by profit, state;


-- 9. Order by STATE in asc , Profit in Desc
select * from STARTUPS
order by state, profit desc;

-- 10. Find out different states counts
select state, count(state) from startups
group by state;
-- 11. Find out average profit based on states and arange avg profit in desc order
select avg(profit) as avgprofit, state from startups
group by state order by avgprofit desc;

-- 12. Find out Max MKT based on states and arrange MKT in ascending order
select max(mkt) as maxmkt, state from startups
group by state order by maxmkt;

-- 13. Find out total Spend by startups
select sum(mkt) as totalspend from startups
-- 14. Find out min total spend based on states 
select state,min(mkt) as totalspend from startups
group by state order by totalspend;

-- 15. view tables
select * from tips;
-- 16. view the tips table

select * from tips;
-- 17. Find avg of total bill based on day and time
select Day, Time, avg(total_bill) as totalbill from tips
group by Day, Time order by totalbill;

-- 18. Find out sum of total bill and tips based on smoker and gender 
-- order by tips desc
select smoker, gender, sum(total_bill) as totalbill, sum(tip) as totaltips from tips
group by smoker, gender order by totalbill;

-- 19. Find out top 5 tips in the data
select top 5 tip  from tips
order by tip  desc;
-- 20. Find out bottom 3 total_bill in the data
select top 3 total_bill from tips
order by total_bill ;

-- 21. Find out highest size in the data
select max(size) from tips;

-- 22. Find out highest total bill
select max(total_bill) from tips

-- 23. Find out highest tip by female and non smoker
select max(tip), smoker, gender from tips
where smoker=0 and gender='female'
group by smoker, gender;

-- 24. Find out third highest tip by female and non smoker
select tip, smoker, gender from tips
where smoker=0 and gender='female'
order by tip desc
offset 2 rows fetch next 1 row only;


-- 25. Find out the entry where lowest tip was paid
select min(tip) as lowesttip from tips;
select * from tips
where tip=1;


-- 26. Nested query
select * from tips
where tip=(select min(tip) as lowesttip from tips);

-- 27. Find out 5th lowest tip paid by female, smoker
select tip, smoker, gender from tips
where smoker=1 and gender='female'
order by tip desc
offset 4 rows fetch next 1 row only;




