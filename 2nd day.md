


## 🔹 STEP 1: DATABASE

```sql
CREATE DATABASE training_db;
USE training_db;
```

---

## 🔹 STEP 2: ONE TABLE (EMPLOYEES)

```sql
CREATE TABLE employees (
    emp_id INT PRIMARY KEY AUTO_INCREMENT,
    emp_name VARCHAR(50) NOT NULL,
    department VARCHAR(30),
    salary INT,
    age INT,
    city VARCHAR(30),
    joining_date DATE
);
```

---

##  STEP 3: RAW DATA (DO NOT SKIP)

```sql
INSERT INTO employees
(emp_name, department, salary, age, city, joining_date)
VALUES
('Rahul Sharma', 'IT', 45000, 25, 'Pune', '2022-03-10'),
('Amit Verma', 'HR', 38000, 28, 'Mumbai', '2021-07-15'),
('Neha Singh', 'IT', 52000, 26, 'Delhi', '2023-01-05'),
('Priya Patil', 'Finance', 60000, 30, 'Pune', '2020-11-20'),
('Rohit Kumar', 'IT', 48000, 24, 'Bangalore', '2022-06-18'),
('Sneha Joshi', 'HR', 35000, 27, 'Pune', '2023-02-12'),
('Ankit Mehta', 'Finance', 70000, 35, 'Mumbai', '2019-09-01'),
('Kiran Rao', 'IT', 55000, 29, 'Hyderabad', '2021-12-25'),
('Pooja Deshmukh', 'HR', 40000, 26, 'Nagpur', '2022-08-30'),
('Saurabh Jain', 'IT', 65000, 32, 'Indore', '2020-05-14');
```

---

#  DAY 2 TASKS (CORE SQL PRACTICE)

### 🔸 SELECT PRACTICE

1. Employees table ka **poora data** dikhao
2. Sirf `emp_name`, `salary`, `city` dikhao
3. Sirf **IT department** ke employees dikhao
4. Jinki salary **50000 se zyada** hai unko dikhao
5. Jinki city **Pune** hai aur department **HR** hai
6. Jinki age **25 se kam** hai
7. Sirf **Finance department** ke naam aur salary dikhao

---

### 🔸 UPDATE PRACTICE

8. `Rahul Sharma` ki salary **50000** karo
9. HR department ki salary **3000 se increase** karo
10. `Neha Singh` ki city **Noida** karo
11. Jinki age **30 se zyada** hai unki salary **10% increase** karo

---

### 🔸 DELETE PRACTICE

12. `Nagpur` city wale employee ko delete karo
13. Jinki salary **35000 se kam** hai unko delete karo

---

### 🔸 ALTER PRACTICE

14. Table mein column add karo `experience INT`
15. `salary` ka datatype **BIGINT** karo
16. `experience` column delete karo

---

### 🔸 CHANGE COLUMN

17. `emp_name` ko rename karke `full_name` karo

**Table:** `employees`

---

## 🔸 SELECT PRACTICE – ANSWERS

### 1. Display all employees

```sql
SELECT * FROM employees;
```

---

### 2. Display emp_name, salary, city

```sql
SELECT emp_name, salary, city FROM employees;
```

---

### 3. Display only IT department employees

```sql
SELECT * FROM employees
WHERE department = 'IT';
```

---

### 4. Display employees with salary > 50,000

```sql
SELECT * FROM employees
WHERE salary > 50000;
```

---

### 5. Employees from Pune and HR department

```sql
SELECT * FROM employees
WHERE city = 'Pune' AND department = 'HR';
```

---

### 6. Employees whose age < 25

```sql
SELECT * FROM employees
WHERE age < 25;
```

---

### 7. Finance department names and salaries

```sql
SELECT emp_name, salary FROM employees
WHERE department = 'Finance';
```

---

## 🔸 UPDATE PRACTICE – ANSWERS

### 8. Update Rahul Sharma salary to 50,000

```sql
UPDATE employees
SET salary = 50000
WHERE emp_name = 'Rahul Sharma';
```

---

### 9. Increase HR department salary by 3,000

```sql
UPDATE employees
SET salary = salary + 3000
WHERE department = 'HR';
```

---

### 10. Change Neha Singh city to Noida

```sql
UPDATE employees
SET city = 'Noida'
WHERE emp_name = 'Neha Singh';
```

---

### 11. Increase salary by 10% where age > 30

```sql
UPDATE employees
SET salary = salary * 1.10
WHERE age > 30;
```

---

## 🔸 DELETE PRACTICE – ANSWERS

### 12. Delete employee from Nagpur

```sql
DELETE FROM employees
WHERE city = 'Nagpur';
```

---

### 13. Delete employees with salary < 35,000

```sql
DELETE FROM employees
WHERE salary < 35000;
```

---

## 🔸 ALTER PRACTICE – ANSWERS

### 14. Add experience column

```sql
ALTER TABLE employees
ADD COLUMN experience INT;
```

---

### 15. Change salary datatype to BIGINT

```sql
ALTER TABLE employees
MODIFY COLUMN salary BIGINT;
```

---

### 16. Delete experience column

```sql
ALTER TABLE employees
DROP COLUMN experience;
```

---

## 🔸 CHANGE COLUMN – ANSWER

### 17. Rename emp_name to full_name

```sql
ALTER TABLE employees
CHANGE emp_name full_name VARCHAR(50);
```




Below is the **clean English version** of the Day 3 tasks and their **SQL answers**.
No icons, no emojis.

---

DAY 3 – FILTERING & SORTING
Table used: `employees`

---

WHERE + OPERATORS (Tasks)

1. Display employees whose salary is between 45,000 and 60,000
2. Display employees who live in Pune or Mumbai
3. Display employees who are not from the IT department
4. Display employees whose name starts with 'A'
5. Display employees whose name ends with 'a'

---

ORDER BY (Sorting Tasks)

6. Display employees sorted by salary in ascending order
7. Display employees sorted by salary in descending order
8. Display employees sorted by age from youngest to oldest

---

LIMIT (Top and Bottom)

9. Display the top 3 employees with the highest salaries
10. Display the employee with the lowest salary

---

DATE PRACTICE

11. Display employees who joined after the year 2022
12. Display employees who joined before the year 2020

---

SQL ANSWERS

1. Salary between 45,000 and 60,000

```sql
SELECT * FROM employees
WHERE salary BETWEEN 45000 AND 60000;
```

2. Employees from Pune or Mumbai

```sql
SELECT * FROM employees
WHERE city IN ('Pune', 'Mumbai');
```

3. Employees not from IT department

```sql
SELECT * FROM employees
WHERE department <> 'IT';
```

4. Name starts with 'A'

```sql
SELECT * FROM employees
WHERE emp_name LIKE 'A%';
```

5. Name ends with 'a'

```sql
SELECT * FROM employees
WHERE emp_name LIKE '%a';
```

6. Salary ascending order

```sql
SELECT * FROM employees
ORDER BY salary ASC;
```

7. Salary descending order

```sql
SELECT * FROM employees
ORDER BY salary DESC;
```

8. Youngest employees first

```sql
SELECT * FROM employees
ORDER BY age ASC;
```

9. Top 3 highest salary employees

```sql
SELECT * FROM employees
ORDER BY salary DESC
LIMIT 3;
```

10. Lowest salary employee

```sql
SELECT * FROM employees
ORDER BY salary ASC
LIMIT 1;
```

11. Employees who joined after 2022

```sql
SELECT * FROM employees
WHERE YEAR(joining_date) > 2022;
```

12. Employees who joined before 2020

```sql
SELECT * FROM employees
WHERE YEAR(joining_date) < 2020;
```










