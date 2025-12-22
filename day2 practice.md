



* Strong SELECT / UPDATE / DELETE
* ALTER, CHANGE, TRUNCATE understanding


---

## 🔹 STEP 1: DATABASE

```sql
CREATE DATABASE training_day2;
USE training_day2;
```

---

## 🔹 STEP 2: TABLE (EMPLOYEES)

```sql
CREATE TABLE employees (
    emp_id INT PRIMARY KEY AUTO_INCREMENT,
    emp_name VARCHAR(50) NOT NULL,
    department VARCHAR(30),
    designation VARCHAR(40),
    salary INT,
    age INT,
    city VARCHAR(30),
    joining_date DATE
);
```

---



```sql
INSERT INTO employees
(emp_name, department, designation, salary, age, city, joining_date)
VALUES
('Rahul Sharma', 'IT', 'Developer', 45000, 25, 'Pune', '2022-03-10'),
('Amit Verma', 'HR', 'HR Executive', 38000, 28, 'Mumbai', '2021-07-15'),
('Neha Singh', 'IT', 'Developer', 52000, 26, 'Delhi', '2023-01-05'),
('Priya Patil', 'Finance', 'Accountant', 60000, 30, 'Pune', '2020-11-20'),
('Rohit Kumar', 'IT', 'Tester', 48000, 24, 'Bangalore', '2022-06-18'),
('Sneha Joshi', 'HR', 'Recruiter', 35000, 27, 'Pune', '2023-02-12'),
('Ankit Mehta', 'Finance', 'Manager', 70000, 35, 'Mumbai', '2019-09-01'),
('Kiran Rao', 'IT', 'Developer', 55000, 29, 'Hyderabad', '2021-12-25'),
('Pooja Deshmukh', 'HR', 'HR Executive', 40000, 26, 'Nagpur', '2022-08-30'),
('Saurabh Jain', 'IT', 'Team Lead', 65000, 32, 'Indore', '2020-05-14'),
('Vikas Malhotra', 'Sales', 'Sales Executive', 42000, 27, 'Delhi', '2021-10-10'),
('Rina Kapoor', 'Sales', 'Sales Manager', 58000, 34, 'Mumbai', '2019-04-22'),
('Manish Gupta', 'IT', 'Support Engineer', 36000, 23, 'Jaipur', '2023-03-01'),
('Kavita Nair', 'Finance', 'Analyst', 54000, 28, 'Kochi', '2022-01-17'),
('Arjun Reddy', 'IT', 'Developer', 50000, 26, 'Chennai', '2021-06-05');
```

#  DAY 2 PRACTICE QUESTIONS (25 QUESTIONS)

## 🔸 PART 1: BASIC SELECT

1. Display all employees
2. Display only emp_name, department, and salary
3. Display employees who belong to the IT department
4. Display employees who live in Pune
5. Display employees whose salary is greater than 50,000

---

## 🔸 PART 2: WHERE CONDITIONS

6. Display employees whose age is less than 26
7. Display employees from HR department and Pune city
8. Display employees whose salary is between 40,000 and 60,000
9. Display employees who joined after 2022-01-01
10. Display employees whose designation is Developer

---

## 🔸 PART 3: UPDATE PRACTICE

11. Update salary of Rahul Sharma to 48,000
12. Increase salary by 3,000 for all HR employees
13. Change city of Neha Singh to Noida
14. Increase salary by 10% for employees whose age is greater than 30
15. Change designation of Rohit Kumar to “Senior Tester”

---

## 🔸 PART 4: DELETE PRACTICE

16. Delete the employee who belongs to Nagpur
17. Delete employees whose salary is less than 38,000
18. Delete employees who joined before 2020-01-01

---

## 🔸 PART 5: ALTER TABLE PRACTICE

19. Add a new column `email VARCHAR(100)`
20. Add a new column `experience INT`
21. Modify salary column datatype to BIGINT
22. Drop the column `experience`

---

## 🔸 PART 6: CHANGE, TRUNCATE, DROP

23. Rename column `emp_name` to `full_name`
24. Remove all records from the employees table using TRUNCATE
25. Delete the employees table completely using DROP


