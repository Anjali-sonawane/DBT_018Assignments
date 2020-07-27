Sameer Dehadrai Page: 1
Assignment – 15
Using Subqueries with DML Commands.
1) Assume there is a table called Multicust, with all of the same column definitions as Salespeople.
 Write a command that inserts all salespeople with more than one customer into this table.

CREATE TABLE Multicast AS
SELECT *
FROM salespeople
WHERE snum IN
    (SELECT snum
     FROM customers
     GROUP BY snum
     HAVING count(snum)>1);
	 

2) Write a command that deletes all customers with no current orders.


DELETE customers
WHERE cnum=ANY
    (SELECT cnum
     FROM orders
     WHERE cnum NOT IN
         (SELECT cnum
          FROM customers));

3) Write a command that increases by twenty percent the commissions of all salespeople with total orders above Rs. 3,000.
UPDATE salespeople
SET comm=comm*1.20
WHERE snum IN
    (SELECT snum
     FROM orders
     WHERE amt>300);
