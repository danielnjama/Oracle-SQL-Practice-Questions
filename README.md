# Oracle SQL Practice Questions

This document provides a set of practice questions to help you improve your Oracle SQL skills. It includes a sample table creation script, sample data, and a series of questions with expected outputs.

## Table Creation and Sample Data

First, let's create a sample table and insert some data into it.

```sql
-- Create the Employees table
CREATE TABLE Employees (
    EmployeeID NUMBER PRIMARY KEY,
    FirstName VARCHAR2(50),
    LastName VARCHAR2(50),
    Department VARCHAR2(50),
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












