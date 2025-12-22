
### (CRUD • ALTER • TABLE OPERATIONS)



## 🔹 STEP 1: DATABASE

```sql
CREATE DATABASE college_db;
USE college_db;
```

---

## 🔹 STEP 2: TABLE (STUDENTS)

```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY AUTO_INCREMENT,
    student_name VARCHAR(50) NOT NULL,
    course VARCHAR(40),
    age INT,
    fees INT,
    city VARCHAR(30),
    admission_date DATE
);
```

---

## 🔹 STEP 3: RAW DATA (FOR PRACTICE)

```sql
INSERT INTO students
(student_name, course, age, fees, city, admission_date)
VALUES
('Amit Kumar', 'BCA', 20, 45000, 'Delhi', '2022-07-15'),
('Neha Sharma', 'BSc', 19, 40000, 'Pune', '2023-01-10'),
('Rahul Verma', 'BCA', 21, 48000, 'Mumbai', '2021-06-20'),
('Priya Singh', 'BCom', 22, 42000, 'Delhi', '2020-08-05'),
('Suresh Patil', 'BSc', 20, 41000, 'Pune', '2022-09-12'),
('Anjali Mehta', 'BCA', 19, 46000, 'Ahmedabad', '2023-02-18'),
('Rohit Jain', 'BCom', 23, 39000, 'Indore', '2021-11-25'),
('Kiran Joshi', 'BSc', 21, 43000, 'Nagpur', '2020-07-30');
```

---

# ✅ DAY 2 TASKS

## 🔸 PART 1: SELECT PRACTICE

1. Display **all students**
2. Display only **student_name, course, and fees**
3. Display students enrolled in **BCA course**
4. Display students whose **fees are greater than 45,000**
5. Display students from **Delhi city**
6. Display students whose **age is less than 21**
7. Display students enrolled in **BSc** and from **Pune**

---

## 🔸 PART 2: UPDATE PRACTICE

8. Update fees of **Amit Kumar** to **47,000**
9. Increase fees by **2,000** for all **BSc students**
10. Change city of **Rahul Verma** to **Noida**
11. Increase fees by **10%** for students whose age is **greater than 21**

---

## 🔸 PART 3: DELETE PRACTICE

12. Delete the student who belongs to **Nagpur**
13. Delete students whose **fees are less than 40,000**

---

## 🔸 PART 4: ALTER TABLE PRACTICE

14. Add a new column `email VARCHAR(100)`
15. Change the datatype of `fees` to **BIGINT**
16. Drop the column `email`

---

## 🔸 PART 5: CHANGE COLUMN

17. Rename column `student_name` to `full_name`

---

## 🔸 PART 6: TRUNCATE & DROP

18. Remove all records from the students table using **TRUNCATE**
19. Delete the students table completely using **DROP**



---

# SQL DAY 2 – ANSWERS

**Table:** `students`

---

## 🔸 PART 1: SELECT – ANSWERS

### 1. Display all students

```sql
SELECT * FROM students;
```

### 2. Display student_name, course, and fees

```sql
SELECT student_name, course, fees FROM students;
```

### 3. Students enrolled in BCA

```sql
SELECT * FROM students
WHERE course = 'BCA';
```

### 4. Students with fees greater than 45,000

```sql
SELECT * FROM students
WHERE fees > 45000;
```

### 5. Students from Delhi

```sql
SELECT * FROM students
WHERE city = 'Delhi';
```

### 6. Students whose age is less than 21

```sql
SELECT * FROM students
WHERE age < 21;
```

### 7. BSc students from Pune

```sql
SELECT * FROM students
WHERE course = 'BSc' AND city = 'Pune';
```

---

## 🔸 PART 2: UPDATE – ANSWERS

### 8. Update fees of Amit Kumar to 47,000

```sql
UPDATE students
SET fees = 47000
WHERE student_name = 'Amit Kumar';
```

---

### 9. Increase fees by 2,000 for all BSc students

```sql
UPDATE students
SET fees = fees + 2000
WHERE course = 'BSc';
```

---

### 10. Change city of Rahul Verma to Noida

```sql
UPDATE students
SET city = 'Noida'
WHERE student_name = 'Rahul Verma';
```

---

### 11. Increase fees by 10% where age > 21

```sql
UPDATE students
SET fees = fees * 1.10
WHERE age > 21;
```

---

## 🔸 PART 3: DELETE – ANSWERS

### 12. Delete student from Nagpur

```sql
DELETE FROM students
WHERE city = 'Nagpur';
```

---

### 13. Delete students with fees less than 40,000

```sql
DELETE FROM students
WHERE fees < 40000;
```

---

## 🔸 PART 4: ALTER TABLE – ANSWERS

### 14. Add email column

```sql
ALTER TABLE students
ADD COLUMN email VARCHAR(100);
```

---

### 15. Change datatype of fees to BIGINT

```sql
ALTER TABLE students
MODIFY COLUMN fees BIGINT;
```

---

### 16. Drop email column

```sql
ALTER TABLE students
DROP COLUMN email;
```

---

## 🔸 PART 5: CHANGE COLUMN – ANSWER

### 17. Rename student_name to full_name

```sql
ALTER TABLE students
CHANGE student_name full_name VARCHAR(50);
```

---

## 🔸 PART 6: TRUNCATE & DROP – ANSWERS

### 18. Remove all records (table remains)

```sql
TRUNCATE TABLE students;
```

---

### 19. Delete table completely

```sql
DROP TABLE students;
```

---

#  IMPORTANT DAY 2 TAKEAWAYS

* `WHERE` is **mandatory** for UPDATE & DELETE
* `TRUNCATE` removes data, keeps structure
* `DROP` removes everything
* `CHANGE` is used to rename columns (MySQL)

---





I’ll continue in the same professional learning flow.
