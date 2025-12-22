
#  SQL PRACTICE SHEET

## (ONE TABLE – DAY 2 & DAY 3)

---

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

## 🔹 STEP 3: RAW DATA (DO NOT SKIP)

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

---

# ✅ DAY 3 TASKS (FILTERING & SORTING)

### 🔸 WHERE + OPERATORS

1. Jinki salary **45000 aur 60000 ke beech** hai
2. Jinki city **Pune ya Mumbai** hai
3. Jinki department **IT nahi** hai
4. Jinka naam **'A' se start** hota hai
5. Jinka naam **'a' pe end** hota hai

---

### 🔸 ORDER BY

6. Salary ke basis pe **ascending order**
7. Salary ke basis pe **descending order**
8. Age ke basis pe **youngest first**

---

### 🔸 LIMIT

9. Top **3 highest salary** wale employees
10. Sabse **kam salary** wala employee

---

### 🔸 DATE PRACTICE

11. Jo **2022 ke baad join** hue hain
12. Jo **2020 se pehle join** hue hain

---

## 🎯 RULES FOR YOU

* Har task ki **SQL query khud likho**
* Output dekho
* Galti aayi → wahi learning hai


