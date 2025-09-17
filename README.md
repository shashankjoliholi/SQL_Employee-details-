# Employee Queries using Oracle SQL

## Project Overview
This mini project demonstrates retrieving data from an existing Oracle Database employee table using basic SQL queries. The focus is on:

- **SELECT**: Retrieve all data from the table  
- **SELECTION (WHERE clause)**: Filter data based on conditions  
- **PROJECTION**: Select specific columns  

## Technologies Used
- Oracle SQL (SQL*Plus)

## Table Structure
| Column Name | Description |
|-------------|-------------|
| EMPNO | Employee Number |
| ENAME | Employee Name |
| JOB | Job Role |
| MGR | Manager ID |
| HIREDATE | Hiring Date |
| SAL | Salary |
| COMM | Commission |
| DEPTNO | Department Number |

## Sample Data
| EMPNO | ENAME | JOB | MGR | HIREDATE | SAL | COMM | DEPTNO |
|-------|--------|-----------|------|-----------|------|-------|--------|
| 7369 | SMITH | CLERK | 7902 | 17-DEC-80 | 800 | | 20 |
| 7499 | ALLEN | SALESMAN | 7698 | 20-FEB-81 | 1600 | 300 | 30 |
| 7521 | WARD | SALESMAN | 7698 | 22-FEB-81 | 1250 | 500 | 30 |
| 7566 | JONES | MANAGER | 7839 | 02-APR-81 | 2975 | | 20 |
| 7654 | MARTIN | SALESMAN | 7698 | 28-SEP-81 | 1250 | 1400 | 30 |
| 7698 | BLAKE | MANAGER | 7839 | 01-MAY-81 | 2850 | | 30 |
| 7782 | CLARK | MANAGER | 7839 | 09-JUN-81 | 2450 | | 10 |
| 7788 | SCOTT | ANALYST | 7566 | 19-APR-87 | 3000 | | 20 |
| 7839 | KING | PRESIDENT | | 17-NOV-81 | 5000 | | 10 |
| 7844 | TURNER | SALESMAN | 7698 | 08-SEP-81 | 1500 | 0 | 30 |
| 7876 | ADAMS | CLERK | 7788 | 23-MAY-87 | 1100 | | 20 |
| 7900 | JAMES | CLERK | 7698 | 03-DEC-81 | 950 | | 30 |
| 7902 | FORD | ANALYST | 7566 | 03-DEC-81 | 3000 | | 20 |
| 7934 | MILLER | CLERK | 7782 | 23-JAN-82 | 1300 | | 10 |

## Sample Queries
```sql
-- Retrieve all employee details
SELECT * FROM EMP;

-- Projection: Select only employee name, job, and salary
SELECT ENAME, JOB, SAL FROM EMP;

-- Selection: Employees with salary greater than 3000
SELECT * FROM EMP WHERE SAL > 3000;

-- Selection + Projection: Names and jobs of employees in department 10
SELECT ENAME, JOB FROM EMP WHERE DEPTNO = 10;
