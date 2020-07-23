use sales;
show tables;
select * from salespeople;
select * from customers;
select * from orders;
1.select onum,cname from orders,customers where orders.cnum = customers.cnum  order by onum;

2.select sname,cname ,onum from orders,customers,salespeople 
where orders.snum = customers.snum and orders.snum =salespeople.snum;

3.select cname,sname ,comm * 100 as "rate of comm"  from salespeople,customers 
where customers.snum = salespeople.snum and comm > 0.12;  



4.select amt,comm from salespeople,orders,customers 
where rating>100 and customers.snum=salespeople.snum and orders.snum=salespeople.snum;

