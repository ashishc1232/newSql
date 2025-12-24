
## 1. Table: `employees`

### Table Structure

```sql
CREATE TABLE employees (
    emp_id INT PRIMARY KEY,
    emp_name VARCHAR(50),
    department VARCHAR(30),
    designation VARCHAR(30),
    salary INT,
    join_date DATE,
    city VARCHAR(30)
);
```

---

## 2. Insert Good Sample Data

```sql
INSERT INTO employees VALUES
(101, 'Amit',   'IT',       'Developer', 60000, '2021-03-15', 'Pune'),
(102, 'Ravi',   'HR',       'Manager',   55000, '2020-07-10', 'Mumbai'),
(103, 'Neha',   'IT',       'Tester',    45000, '2022-01-20', 'Pune'),
(104, 'Priya',  'Finance',  'Analyst',   65000, '2019-11-05', 'Delhi'),
(105, 'Suresh', 'IT',       'Developer', 70000, '2018-06-18', 'Bangalore'),
(106, 'Kiran',  'HR',       'Executive', 40000, '2021-09-25', 'Mumbai'),
(107, 'Anjali', 'Finance',  'Manager',   80000, '2017-04-12', 'Delhi'),
(108, 'Rahul',  'Sales',    'Executive', 42000, '2022-08-01', 'Chennai'),
(109, 'Vikas',  'Sales',    'Manager',   75000, '2019-02-14', 'Chennai'),
(110, 'Sneha',  'IT',       'Developer', 68000, '2020-12-30', 'Hyderabad');
```

---

## 3. SQL Clauses Questions (Practice)

### SELECT / WHERE

1. Display all employee details.
2. Display only `emp_name` and `salary`.
3. Find employees whose salary is greater than 60000.
4. List employees from the IT department.
5. Find employees who live in Mumbai.

### AND / OR / NOT

6. Find employees from IT department **and** salary above 65000.
7. List employees from HR **or** Finance department.
8. Display employees who are **not** from Pune.

### BETWEEN / IN / LIKE

9. Find employees whose salary is between 45000 and 70000.
10. Display employees whose city is in Pune, Delhi, or Mumbai.
11. Find employees whose name starts with 'A'.
12. Find employees whose name contains 'h'.

### ORDER BY

13. Display employees ordered by salary ascending.
14. Display employees ordered by join_date descending.
15. Sort employees by department and then salary descending.

### DISTINCT / LIMIT

16. Display distinct departments.
17. Display top 5 highest paid employees.

---

## 4. Aggregate Function Questions (Asked at the End)

### Basic Aggregates

18. Find total number of employees.
19. Find minimum salary.
20. Find maximum salary.
21. Find average salary of all employees.
22. Find total salary paid to all employees.

### GROUP BY

23. Find department-wise total salary.
24. Find department-wise average salary.
25. Count number of employees in each department.
26. Find city-wise employee count.

### HAVING

27. Display departments where average salary is greater than 60000.
28. Display cities having more than 2 employees.
29. Find departments where total salary exceeds 150000.




## 1–17 : Clauses Answers

```sql
-- 1
SELECT * FROM employees;

-- 2
SELECT emp_name, salary FROM employees;

-- 3
SELECT * FROM employees
WHERE salary > 60000;

-- 4
SELECT * FROM employees
WHERE department = 'IT';

-- 5
SELECT * FROM employees
WHERE city = 'Mumbai';

-- 6
SELECT * FROM employees
WHERE department = 'IT' AND salary > 65000;

-- 7
SELECT * FROM employees
WHERE department = 'HR' OR department = 'Finance';

-- 8
SELECT * FROM employees
WHERE city <> 'Pune';

-- 9
SELECT * FROM employees
WHERE salary BETWEEN 45000 AND 70000;

-- 10
SELECT * FROM employees
WHERE city IN ('Pune', 'Delhi', 'Mumbai');

-- 11
SELECT * FROM employees
WHERE emp_name LIKE 'A%';

-- 12
SELECT * FROM employees
WHERE emp_name LIKE '%h%';

-- 13
SELECT * FROM employees
ORDER BY salary ASC;

-- 14
SELECT * FROM employees
ORDER BY join_date DESC;

-- 15
SELECT * FROM employees
ORDER BY department, salary DESC;

-- 16
SELECT DISTINCT department FROM employees;

-- 17
SELECT * FROM employees
ORDER BY salary DESC
LIMIT 5;
```

---

## 18–29 : Aggregate Answers

```sql
-- 18
SELECT COUNT(*) FROM employees;

-- 19
SELECT MIN(salary) FROM employees;

-- 20
SELECT MAX(salary) FROM employees;

-- 21
SELECT AVG(salary) FROM employees;

-- 22
SELECT SUM(salary) FROM employees;

-- 23
SELECT department, SUM(salary)
FROM employees
GROUP BY department;

-- 24
SELECT department, AVG(salary)
FROM employees
GROUP BY department;

-- 25
SELECT department, COUNT(*)
FROM employees
GROUP BY department;

-- 26
SELECT city, COUNT(*)
FROM employees
GROUP BY city;

-- 27
SELECT department, AVG(salary)
FROM employees
GROUP BY department
HAVING AVG(salary) > 60000;

-- 28
SELECT city, COUNT(*)
FROM employees
GROUP BY city
HAVING COUNT(*) > 2;

-- 29
SELECT department, SUM(salary)
FROM employees
GROUP BY department
HAVING SUM(salary) > 150000;
```



