# Oracle SQL Practice Questions

This document provides a set of practice questions to help you improve your Oracle SQL skills. It includes a sample table creation script, sample data, and a series of questions with expected outputs.

## Table Creation and Sample Data

First, let's create a sample table and insert some data into it.

```sql
-- Create the Employees table
CREATE TABLE Employees (
    EmployeeID NUMBER PRIMARY KEY,
    FirstName VARCHAR2(15),
    LastName VARCHAR2(15),
    Department VARCHAR2(15),
    Salary NUMBER,
    HireDate DATE
);

-- Insert sample data into the Employees table
INSERT INTO Employees (EmployeeID, FirstName, LastName, Department, Salary, HireDate) VALUES (1, 'John', 'Doe', 'IT', 60000, TO_DATE('2020-01-15', 'YYYY-MM-DD'));
INSERT INTO Employees (EmployeeID, FirstName, LastName, Department, Salary, HireDate) VALUES (2, 'Jane', 'Smith', 'HR', 55000, TO_DATE('2019-03-22', 'YYYY-MM-DD'));
INSERT INTO Employees (EmployeeID, FirstName, LastName, Department, Salary, HireDate) VALUES (3, 'Alice', 'Johnson', 'IT', 65000, TO_DATE('2021-07-10', 'YYYY-MM-DD'));
INSERT INTO Employees (EmployeeID, FirstName, LastName, Department, Salary, HireDate) VALUES (4, 'Bob', 'Brown', 'Finance', 70000, TO_DATE('2018-05-30', 'YYYY-MM-DD'));
INSERT INTO Employees (EmployeeID, FirstName, LastName, Department, Salary, HireDate) VALUES (5, 'Charlie', 'Davis', 'HR', 50000, TO_DATE('2022-02-01', 'YYYY-MM-DD'));
INSERT INTO Employees (EmployeeID, FirstName, LastName, Department, Salary, HireDate) VALUES (6, 'Eva', 'Green', 'Finance', 72000, TO_DATE('2020-11-15', 'YYYY-MM-DD'));


Practice Questions
Question 1: Retrieve all columns from the Employees table.
Expected Output:
EMPLOYEEID | FIRSTNAME | LASTNAME | DEPARTMENT | SALARY | HIREDATE
-----------|-----------|----------|------------|--------|---------
1          | John      | Doe      | IT         | 60000  | 15-JAN-20
2          | Jane      | Smith    | HR         | 55000  | 22-MAR-19
3          | Alice     | Johnson  | IT         | 65000  | 10-JUL-21
4          | Bob       | Brown    | Finance    | 70000  | 30-MAY-18
5          | Charlie   | Davis    | HR         | 50000  | 01-FEB-22
6          | Eva       | Green    | Finance    | 72000  | 15-NOV-20

Question 2: Retrieve the FirstName, LastName, and Salary of all employees in the IT department.
Expected Output:
FIRSTNAME | LASTNAME | SALARY
----------|----------|-------
John      | Doe      | 60000
Alice     | Johnson  | 65000

Question 3: Retrieve the total number of employees in each department.
Expected Output:
DEPARTMENT | EMPLOYEE_COUNT
-----------|---------------
IT         | 2
HR         | 2
Finance    | 2

Question 4: Retrieve the highest salary in the Employees table.
Expected Output:
MAX_SALARY
----------
72000

Question 5: Retrieve the names of employees who were hired after January 1, 2020.
Expected Output:
FIRSTNAME | LASTNAME
----------|----------
John      | Doe
Alice     | Johnson
Charlie   | Davis
Eva       | Green

Question 6: Retrieve the average salary of employees in the HR department.
Expected Output:
AVG_SALARY
-----------
52500

Question 7: Retrieve the employees who earn more than the average salary in their department.
Expected Output:
EMPLOYEEID | FIRSTNAME | LASTNAME | DEPARTMENT | SALARY | HIREDATE
-----------|-----------|----------|------------|--------|---------
1          | John      | Doe      | IT         | 60000  | 15-JAN-20
3          | Alice     | Johnson  | IT         | 65000  | 10-JUL-21
4          | Bob       | Brown    | Finance    | 70000  | 30-MAY-18
6          | Eva       | Green    | Finance    | 72000  | 15-NOV-20

Question 8: Retrieve the employees who have the highest salary in their respective departments.
Expected Output:
EMPLOYEEID | FIRSTNAME | LASTNAME | DEPARTMENT | SALARY | HIREDATE
-----------|-----------|----------|------------|--------|---------
3          | Alice     | Johnson  | IT         | 65000  | 10-JUL-21
2          | Jane      | Smith    | HR         | 55000  | 22-MAR-19
6          | Eva       | Green    | Finance    | 72000  | 15-NOV-20

Question 9: Retrieve the employees who have been with the company for more than 2 years.
Expected Output:
EMPLOYEEID | FIRSTNAME | LASTNAME | DEPARTMENT | SALARY | HIREDATE
-----------|-----------|----------|------------|--------|---------
1          | John      | Doe      | IT         | 60000  | 15-JAN-20
2          | Jane      | Smith    | HR         | 55000  | 22-MAR-19
4          | Bob       | Brown    | Finance    | 70000  | 30-MAY-18
6          | Eva       | Green    | Finance    | 72000  | 15-NOV-20

Question 10: Retrieve the employees who have the same salary.
Expected Output:
SALARY | EMPLOYEEID | FIRSTNAME | LASTNAME | DEPARTMENT | HIREDATE
-------|------------|-----------|----------|------------|---------
55000  | 2          | Jane      | Smith    | HR         | 22-MAR-19
55000  | 5          | Charlie   | Davis    | HR         | 01-FEB-22

-----------------------------------------
2nd pack
-----------------------------------------
-- Create Employees Table
CREATE TABLE Employees (
    EMPLOYEE_ID NUMBER PRIMARY KEY,
    FIRST_NAME VARCHAR2(50),
    LAST_NAME VARCHAR2(50),
    DEPARTMENT_ID NUMBER,
    SALARY NUMBER,
    HIRE_DATE DATE
);

-- Create Departments Table
CREATE TABLE Departments (
    DEPARTMENT_ID NUMBER PRIMARY KEY,
    DEPARTMENT_NAME VARCHAR2(50),
    MANAGER_ID NUMBER
);

-- Create Projects Table
CREATE TABLE Projects (
    PROJECT_ID NUMBER PRIMARY KEY,
    PROJECT_NAME VARCHAR2(100),
    DEPARTMENT_ID NUMBER,
    START_DATE DATE,
    END_DATE DATE
);

-- Insert data into Employees Table
INSERT INTO Employees (EMPLOYEE_ID, FIRST_NAME, LAST_NAME, DEPARTMENT_ID, SALARY, HIRE_DATE)
VALUES (101, 'John', 'Doe', 10, 5000, TO_DATE('2015-06-24', 'YYYY-MM-DD'));

INSERT INTO Employees (EMPLOYEE_ID, FIRST_NAME, LAST_NAME, DEPARTMENT_ID, SALARY, HIRE_DATE)
VALUES (102, 'Jane', 'Smith', 20, 6000, TO_DATE('2017-09-15', 'YYYY-MM-DD'));

INSERT INTO Employees (EMPLOYEE_ID, FIRST_NAME, LAST_NAME, DEPARTMENT_ID, SALARY, HIRE_DATE)
VALUES (103, 'Alice', 'Johnson', 10, 5500, TO_DATE('2018-03-10', 'YYYY-MM-DD'));

INSERT INTO Employees (EMPLOYEE_ID, FIRST_NAME, LAST_NAME, DEPARTMENT_ID, SALARY, HIRE_DATE)
VALUES (104, 'Bob', 'Brown', 30, 4500, TO_DATE('2019-11-05', 'YYYY-MM-DD'));

INSERT INTO Employees (EMPLOYEE_ID, FIRST_NAME, LAST_NAME, DEPARTMENT_ID, SALARY, HIRE_DATE)
VALUES (105, 'Charlie', 'Davis', 20, 7000, TO_DATE('2020-08-12', 'YYYY-MM-DD'));

-- Insert data into Departments Table
INSERT INTO Departments (DEPARTMENT_ID, DEPARTMENT_NAME, MANAGER_ID)
VALUES (10, 'HR', 101);

INSERT INTO Departments (DEPARTMENT_ID, DEPARTMENT_NAME, MANAGER_ID)
VALUES (20, 'IT', 102);

INSERT INTO Departments (DEPARTMENT_ID, DEPARTMENT_NAME, MANAGER_ID)
VALUES (30, 'Finance', 104);

-- Insert data into Projects Table
INSERT INTO Projects (PROJECT_ID, PROJECT_NAME, DEPARTMENT_ID, START_DATE, END_DATE)
VALUES (1, 'HR System', 10, TO_DATE('2021-01-01', 'YYYY-MM-DD'), TO_DATE('2021-12-31', 'YYYY-MM-DD'));

INSERT INTO Projects (PROJECT_ID, PROJECT_NAME, DEPARTMENT_ID, START_DATE, END_DATE)
VALUES (2, 'IT Upgrade', 20, TO_DATE('2022-03-15', 'YYYY-MM-DD'), TO_DATE('2022-09-30', 'YYYY-MM-DD'));

INSERT INTO Projects (PROJECT_ID, PROJECT_NAME, DEPARTMENT_ID, START_DATE, END_DATE)
VALUES (3, 'Finance Audit', 30, TO_DATE('2023-02-01', 'YYYY-MM-DD'), TO_DATE('2023-05-31', 'YYYY-MM-DD'));




1. Retrieve all employees' first names, last names, and salaries.
Expected Output:
FIRST_NAME | LAST_NAME | SALARY
---------------------------------
John       | Doe       | 5000
Jane       | Smith     | 6000
Alice      | Johnson   | 5500
Bob        | Brown     | 4500
Charlie    | Davis     | 7000

2. Find all employees who earn more than 5000.
Expected Output:
FIRST_NAME | LAST_NAME | SALARY
---------------------------------
Jane       | Smith     | 6000
Alice      | Johnson   | 5500
Charlie    | Davis     | 7000

3. List all departments and their managers' first and last names.
Expected Output:
DEPARTMENT_NAME | FIRST_NAME | LAST_NAME
-----------------------------------------
HR              | John       | Doe
IT              | Jane       | Smith
Finance         | Bob        | Brown

4. Retrieve all employees along with their department names.
Expected Output:
FIRST_NAME | LAST_NAME | DEPARTMENT_NAME
-----------------------------------------
John       | Doe       | HR
Jane       | Smith     | IT
Alice      | Johnson   | HR
Bob        | Brown     | Finance
Charlie    | Davis     | IT

5. Find all projects along with the department name and manager's first name.
Expected Output:
PROJECT_NAME | DEPARTMENT_NAME | FIRST_NAME
--------------------------------------------
HR System    | HR              | John
IT Upgrade   | IT              | Jane
Finance Audit| Finance         | Bob

6. Find the total salary expenditure for each department.
Expected Output:
DEPARTMENT_NAME | TOTAL_SALARY
-------------------------------
HR              | 10500
IT              | 13000
Finance         | 4500

7. Find the average salary of employees in each department.
Expected Output:
DEPARTMENT_NAME | AVG_SALARY
-----------------------------
HR              | 5250
IT              | 6500
Finance         | 4500

8. Find employees who earn more than the average salary of their department.
Expected Output:
FIRST_NAME | LAST_NAME | SALARY | DEPARTMENT_NAME
-------------------------------------------------
Jane       | Smith     | 6000   | IT
Charlie    | Davis     | 7000   | IT

9. Find departments that have no employees.
Expected Output:
DEPARTMENT_NAME
----------------
(No rows returned)

10. Find employees hired in the year 2018.
Expected Output:
FIRST_NAME | LAST_NAME | HIRE_DATE
-----------------------------------
Alice      | Johnson   | 2018-03-10

11. Find projects that started in 2022.
Expected Output:
PROJECT_NAME | START_DATE
--------------------------
IT Upgrade   | 2022-03-15

12. Find the second highest salary in the company.
Expected Output:
SECOND_HIGHEST_SALARY
----------------------
6000

13. Find employees who are also managers of a department.
Expected Output:
FIRST_NAME | LAST_NAME | DEPARTMENT_NAME
-----------------------------------------
John       | Doe       | HR
Jane       | Smith     | IT
Bob        | Brown     | Finance

14. Find the longest-running project (by duration in days).
Expected Output:
PROJECT_NAME | DURATION_DAYS
----------------------------
HR System    | 364

15. Rank employees by salary within their department.
Expected Output:
FIRST_NAME | LAST_NAME | SALARY | DEPARTMENT_NAME | SALARY_RANK
---------------------------------------------------------------
Alice      | Johnson   | 5500   | HR              | 1
John       | Doe       | 5000   | HR              | 2
Charlie    | Davis     | 7000   | IT              | 1
Jane       | Smith     | 6000   | IT              | 2
Bob        | Brown     | 4500   | Finance         | 1

16. Find the cumulative salary for each department.
Expected Output:
DEPARTMENT_NAME | FIRST_NAME | LAST_NAME | CUMULATIVE_SALARY
------------------------------------------------------------
HR              | Alice      | Johnson   | 5500
HR              | John       | Doe       | 10500
IT              | Charlie    | Davis     | 7000
IT              | Jane       | Smith     | 13000
Finance         | Bob        | Brown     | 4500

17. Find employees who are not managers of any department.
Expected Output:
FIRST_NAME | LAST_NAME
-----------------------
Alice      | Johnson
Charlie    | Davis

18. Find departments that have both employees and projects.
Expected Output:
DEPARTMENT_NAME
----------------
HR
IT
Finance

19. Insert a new employee into the Employees table.
Expected Output:
(1 rows updated)

20. Update the salary of employees in the IT department by 10%.
Expected Output:
(2 rows updated)

21. Find the number of employees in each department.
Expected Output:
DEPARTMENT_NAME | EMPLOYEE_COUNT
--------------------------------
HR              | 2
IT              | 2
Finance         | 1















