Sameer Dehadrai Page: 1
Assignment – 17
Constraining the Values of your data.
1) Create the Orders table so that all onum values as well as all combinations of cnum and snum are different from one another,
 and so that NULL values are excluded from the date field.


CREATE TABLE orders1 ( onum number(4), cnum number(4), sname number(4), 
						odate date NOT NULL, 
						CONSTRAINT p_k_1 PRIMARY key(onum,cnum,sname) );


2) Create the Salespeople table so that the default commission is 10% with no NULLS permitted,
 snum is the primary key, and all names fall alphabetically between A and M, inclusive (assume all names will be uppercase).

CREATE TABLE salespeople1 (comm int(3) DEFAULT 10,
						snum int(4) PRIMARY KEY,
						sname varchar(10) check(substr(upper(sname),1,1) BETWEEN 'A' AND 'M') );




3) Create the Orders table, making sure that the onum is greater than the cnum, and the cnum is greater that the snum. 
Allow no NULLS in any of these three fields.



CREATE TABLE orders12 ( onum int(4), amt int(7), odate date, cnum int(4), snum int(4), 
						CONSTRAINT on_cn_sn check(onum>cnum AND cnum>snum) 