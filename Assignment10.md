use sales;

select * from customers;
select distinct a.sname,b.sname,b.city from salesperson a,salesperson b where a.city=b.city and a.sname > b.sname;


select cname, city from  customers
WHERE rating =(SELECT rating FROM customers WHERE cname='hoffman');