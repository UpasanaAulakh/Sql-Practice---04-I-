# Sql-Practice---04-I-

create database project
use project

create table Employee_Details(ID int primary key not null,F_Name varchar(20),
L_NAme varchar(20),Salary money,Joining_Date date,Department varchar(20),Gender varchar(20))

select * from Employee_Details
sp_help Employee_details


insert into Employee_Details values
(2,'vikash','ahalabat',60000,'2013-02-15','IT','Male'),
(3,'nikite','jain',53000,'2014-01-09','HR','Female'),
(4,'shweta','sharma',50000,'2013-02-15','IT','Female'),
(5,'moham','rana',60000,'2013-02-15','HR','Male'),
(6,'Raju','ram',45000,'2013-02-20','IT','Male'),
(7,'sanjeev','kumar',60000,'2013-02-15','IT','Male')


select * from Employee_Details where F_Name like '(^a-p)%'

select * from Employee_Details where Gender like '__le'

select * from Employee_Details where F_Name like 'n_____'

select * from Employee_Details where F_Name like '%'

select distinct Department from Employee_Details 

select max(salary) from Employee_Details 
select min(salary) from Employee_Details 
SELECT F_Name, GETDATE() [Current Date], Joining_Date,
DATEDIFF(DD,Joining_Date,GETDATE()) 
AS
[Total Months]
FROM
Employee_details
select*from Employee_Details
where datepart(yyyy,Joining_Date)='2013';
select*from  Employee_Details
where datepart(mm,Joining_Date)='1';
select*from Employee_Details
where Joining_Date between '2014-01-09'and '2015-03-05';
select F_Name case 
when
gender='male'then 'm'
when gender='female'then 'f' find
as
gender from  Employee_Detais
