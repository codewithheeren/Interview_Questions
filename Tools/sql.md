1. what are the difference between sql and nosql database
2. What is ACID properties in database
3.1 What is normalization and denormalization
3.2. explain different sql queries types .
4. What is truncate keyword
5. What is indexing in SQL
6. What is diff b/w primary key and unique key
7.1 select db, create db , use db , drop db
7.2 crud on table
7.3 different constraints in db


Create 2 different tables: Emp Table(Emp ID, Name, DeptId, Country Name, City Name)
Dept Table(Dept Id, Dept Name)

8. Alter the table(add, remove and modify column datatype), rename table
9. IN, NOT IN, BETWEEn, ORDER BY
10. Joins
11. View(Create and Drop)
12. Advantages of views
13. LIKE operator
14. SAVEPOINT, ROLLBACK AND COMMIT
15. GROUP BY
16. HAVING CLAUSE
17. GET EMP with highest salary(second highest, third highest)
18. For each DEPT highest salary

max salary of each department- 
SELECT Dept_name,Emp_name,Emp_salary FROM Employee_Table
INNER JOIN 
Dept_Table
ON Dept_Table.Dept_Id=Employee_Table.Dept_Id
WHERE Emp_salary IN (SELECT MAX(Emp_Salary) FROM Employee_Table GROUP BY Dept_Id);