ASP.NET - Passing Data from Master Page to Content Page



With that programm i pass data from Master Page to Content Page.



1. I use the table Customers with the columns id, Name, Gender, TotalMarks.

use Customers;

create table Customers(
ID int primary key,
Name varchar(50),
Gender varchar(50),
TotalMarks int
)



2. I insert a few data.

Insert into Customers values('Mark Hastings2','Male2',9002)
Insert into Customers values('Mary Ward','Female',870)
Insert into Customers values('Mark Hastings','Male',900)
Insert into Customers values('Mary Ward','Female',870)


3. I create a store procedure to search form the name column. 

Create Proc spSearch
@SearchTerm nvarchar(50)
as
Begin
 Select * from tblStudents where Name like '%' + @SearchTerm + '%'
End


4. I test my store procedure

spSearch 'Ma'


5. I create the Master Page with the name: Site.Master, and i make a search text box with a button.
My goal is to write a name search that in the customer table and then to show the results in the content page with a grid.



6. I put a Grid Control and i write the code to show the results.


please use studentsearch.aspx form 




Katsavaros Konstantinos
