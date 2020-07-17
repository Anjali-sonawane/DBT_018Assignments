# Assignment -2

#### 1) Which field of the Customers table is the primary key?

##### Cnum is primary key of Customers table

 create table CUSTOMERS(
 Cnum int(4),
 Cname varchar(10),
 City varchar(10),
 Rating int(4),
 Snum int(4));
query for making primary key
Alter table customers ADD PRIMARY KEY ( Cnum );

#### 2) What is the 4th column of the Customers table?

##### Rating is the 4th column of Customers table

 create table CUSTOMERS(
 Cnum int(4),
 Cname varchar(10),
 City varchar(10),
 Rating int(4),
 Snum int(4));

#### 3) What is another word for row? For column?

column -------------> attribute
Row -----------------> Entity,opportunity,tuple

### 4) Why isn’t it possible to see the first five rows of a table?