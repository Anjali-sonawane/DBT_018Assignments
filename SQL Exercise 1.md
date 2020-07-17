# SQL Exercise 1

##### 1) Create the table SEMP with the following structure

create table SEMP(EMPNO CHAR(4),
EMPNAME CHAR(20),
BASIC FLOAT(9,2),
DEPTNO CHAR(2),
DEPTHEAD CHAR(4)); 

##### 2) Create the table SDEPT with the following structure

create table SDEPT(
DEPTNO CHAR(2),
DEPTNAME CHAR(15)); 

##### 3) Insert into the SDEPT table the following values

insert into SDEPT values(
10,'Development'),
(20,'Training') 

##### 4) Insert into the SEMP table the following values

insert into SEMP values(0001,'SUNIL',6000,10,'NULL'),
(0002,'HIREN',8000,20,'NULL'),
(0003,'ALI',4000,10,0001),
(0004,'GEORGE',6000,20,0002); 

Create S, P, J, SPJ tables as specified below and insert a few rows in each table

###### SUPPLIER

create table SUPPLIER(S_id varchar(4),
Sname char(20),
status char(4),
City char(10));

insert into SUPPLIER 
values('s1','ram',20,'pune'),
('s2','sham',30,'Abad'),
('s3','sita',10,'nashik');

###### PARTS

create table PARTS( P_id varchar(4),
 Pname char(20),
Color char(10),
Weight varchar(3),
City char(10));

insert into PARTS
values('p1','x','red',20,'pune'),
('p2','y','black',40,'Abad'),
('p3','z','white',30,'nashik');

###### PROJECTS

create table PROJECTS( J_id varchar(4),
Jname char(20),
City char(10));

insert into PROJECTS
values('j1','xxx','pune'),
('j2','yyy','Abad'),
('j3','zzz','nashik');

##### 5) Display all the data from the S table

 select * from SUPPLIER;

##### 6) Display only the S# and SNAME fields from the S table

select Sname from SUPPLIER;

##### 7) Display the PNAME and COLOR from the P table for the CITY=”A”bad

select Pname from PARTS where CITY=”Abad”;

##### 8) Display all the Suppliers from Abad.

select * from SUPPLIER where CITY=”Abad”;

##### 9) Display all the Suppliers from Nashik or Abad

select * from SUPPLIER where CITY=”Abad” or CITY=”pune”;

##### 10) Display all the Projects in Abad.

select * from PROJECTS where CITY=”nashik”;

##### 11) Display all the Part names with the weight between 20and 40(inclusive of both).

select Pname FROM PARTS WHERE Weight BETWEEN 20 AND 40;

##### 12) Display all the Suppliers with a Status greater than or equal to 20.

 select * from  SUPPLIER WHERE Status >= 20;

##### 13) Display all the Suppliers except the Suppliers from Abad.

select * from  SUPPLIER WHERE CITY!="Abad";

##### 14) Display only the Cities from where the Suppliers come from

select city from  SUPPLIER;