
**Table Used:** `employees`
(Use the same table and data provided earlier)

---

## 🔹 PART 1: Advanced WHERE Practice

1. Display employees whose **salary is between 40,000 and 60,000**
2. Display employees whose **age is 25, 26, or 27**
3. Display employees who live in **Pune, Mumbai, or Delhi**
4. Display employees from **IT or Finance** departments
5. Display employees who are **not from the HR department**
6. Display employees who **joined in the year 2022**
7. Display employees whose **salary is less than 50,000** and **age is below 30**

---

## 🔹 PART 2: LIKE & Pattern Matching

8. Display employees whose **name starts with 'R'**
9. Display employees whose **name ends with 'a'**
10. Display employees whose **name contains 'sh'**
11. Display employees whose **name contains the letter 'i'**

---

## 🔹 PART 3: ORDER BY (Sorting)

12. Display employees sorted by **salary in ascending order**
13. Display employees sorted by **salary in descending order**
14. Display employees sorted by **age from youngest to oldest**
15. Display employees sorted by **department name in alphabetical order**

---

## 🔹 PART 4: LIMIT & OFFSET

16. Display the **top 3 employees with the highest salaries**
17. Display the **bottom 2 employees with the lowest salaries**
18. Display the employee with the **second-highest salary**
19. Display the **3rd and 4th records** when sorted by salary

---

## 🔹 PART 5: Aggregate Functions

20. Display the **total number of employees**
21. Display the **maximum salary**
22. Display the **minimum salary**
23. Display the **average salary**
24. Display the **total salary of the IT department**

---

## 🔹 PART 6: GROUP BY Practice

25. Display the **number of employees in each department**
26. Display the **average salary for each department**
27. Display the **number of employees in each city**
28. Display the **highest salary in each department**

---

## 🔹 PART 7: HAVING Clause

29. Display only those departments whose **average salary is greater than 50,000**
30. Display only those cities which have **more than 2 employees**

---




* Filtering
* Sorting
* Aggregate functions
* GROUP BY
* HAVING




#  SQL DAY 3 – PRACTICAL (NEW TABLE & NEW DATA)

##  Day 3 Focus

* WHERE (advanced)
* LIKE
* ORDER BY
* LIMIT / OFFSET
* Aggregate Functions
* GROUP BY
* HAVING

---

## 🔹 STEP 1: DATABASE

```sql
CREATE DATABASE sql_day3;
USE sql_day3;
```

---

## 🔹 STEP 2: TABLE (ORDERS)

```sql
CREATE TABLE orders (
    order_id INT PRIMARY KEY AUTO_INCREMENT,
    customer_name VARCHAR(50),
    product VARCHAR(50),
    category VARCHAR(30),
    quantity INT,
    price INT,
    city VARCHAR(30),
    order_date DATE
);
```

---

## 🔹 STEP 3: RAW DATA (DIFFERENT + REALISTIC)

```sql
INSERT INTO orders
(customer_name, product, category, quantity, price, city, order_date)
VALUES
('Rahul Sharma', 'Laptop', 'Electronics', 1, 55000, 'Pune', '2023-01-10'),
('Neha Singh', 'Mobile', 'Electronics', 2, 40000, 'Delhi', '2023-02-15'),
('Amit Verma', 'Chair', 'Furniture', 4, 12000, 'Mumbai', '2022-11-20'),
('Priya Patil', 'Table', 'Furniture', 1, 18000, 'Pune', '2022-10-05'),
('Rohit Kumar', 'Headphones', 'Electronics', 3, 9000, 'Bangalore', '2023-03-01'),
('Sneha Joshi', 'Shoes', 'Fashion', 2, 6000, 'Pune', '2023-01-25'),
('Ankit Mehta', 'Watch', 'Fashion', 1, 15000, 'Mumbai', '2022-09-18'),
('Kiran Rao', 'Monitor', 'Electronics', 2, 30000, 'Hyderabad', '2023-02-08'),
('Pooja Deshmukh', 'Sofa', 'Furniture', 1, 45000, 'Nagpur', '2022-12-12'),
('Saurabh Jain', 'Camera', 'Electronics', 1, 65000, 'Indore', '2023-03-05'),
('Vikas Malhotra', 'T-Shirt', 'Fashion', 5, 5000, 'Delhi', '2023-01-14'),
('Rina Kapoor', 'Refrigerator', 'Electronics', 1, 72000, 'Mumbai', '2022-08-22'),
('Manish Gupta', 'Shoes', 'Fashion', 3, 9000, 'Jaipur', '2023-02-20'),
('Kavita Nair', 'Dining Set', 'Furniture', 1, 80000, 'Kochi', '2022-07-30'),
('Arjun Reddy', 'Mobile', 'Electronics', 1, 30000, 'Chennai', '2023-03-10');
```

---

#  DAY 3 PRACTICE QUESTIONS (30 QUESTIONS)

## 🔹 PART 1: WHERE (ADVANCED)

1. Display orders where price is between 10,000 and 50,000
2. Display orders where quantity is greater than 2
3. Display orders from Pune or Mumbai
4. Display orders from Electronics category
5. Display orders not from Furniture category
6. Display orders placed in 2023
7. Display orders where price < 20,000 and quantity >= 2

---

## 🔹 PART 2: LIKE PRACTICE

8. Customers whose name starts with ‘R’
9. Customers whose name ends with ‘a’
10. Customers whose name contains ‘sh’
11. Products whose name contains ‘o’

---

## 🔹 PART 3: ORDER BY

12. Sort orders by price (ascending)
13. Sort orders by price (descending)
14. Sort orders by quantity (highest first)
15. Sort orders by city (alphabetical order)

---

## 🔹 PART 4: LIMIT & OFFSET

16. Top 3 most expensive orders
17. Bottom 2 cheapest orders
18. Second highest price order
19. 4th and 5th records based on price

---

## 🔹 PART 5: AGGREGATE FUNCTIONS

20. Total number of orders
21. Maximum order price
22. Minimum order price
23. Average order price
24. Total revenue (price sum)

---

## 🔹 PART 6: GROUP BY

25. Number of orders per category
26. Average price per category
27. Total revenue per city
28. Maximum price per category

---

## 🔹 PART 7: HAVING

29. Categories with average price greater than 40,000
30. Cities with more than 2 orders

---


**Table:** `orders`

---

## 🔹 PART 1: WHERE (ADVANCED)

### 1. Price between 10,000 and 50,000

```sql
SELECT * FROM orders
WHERE price BETWEEN 10000 AND 50000;
```

---

### 2. Quantity greater than 2

```sql
SELECT * FROM orders
WHERE quantity > 2;
```

---

### 3. Orders from Pune or Mumbai

```sql
SELECT * FROM orders
WHERE city IN ('Pune', 'Mumbai');
```

---

### 4. Electronics category orders

```sql
SELECT * FROM orders
WHERE category = 'Electronics';
```

---

### 5. Orders not from Furniture category

```sql
SELECT * FROM orders
WHERE category <> 'Furniture';
```

---

### 6. Orders placed in 2023

```sql
SELECT * FROM orders
WHERE YEAR(order_date) = 2023;
```

---

### 7. Price < 20,000 and quantity ≥ 2

```sql
SELECT * FROM orders
WHERE price < 20000 AND quantity >= 2;
```

---

## 🔹 PART 2: LIKE PRACTICE

### 8. Customer name starts with ‘R’

```sql
SELECT * FROM orders
WHERE customer_name LIKE 'R%';
```

---

### 9. Customer name ends with ‘a’

```sql
SELECT * FROM orders
WHERE customer_name LIKE '%a';
```

---

### 10. Customer name contains ‘sh’

```sql
SELECT * FROM orders
WHERE customer_name LIKE '%sh%';
```

---

### 11. Product name contains ‘o’

```sql
SELECT * FROM orders
WHERE product LIKE '%o%';
```

---

## 🔹 PART 3: ORDER BY

### 12. Sort by price (ascending)

```sql
SELECT * FROM orders
ORDER BY price ASC;
```

---

### 13. Sort by price (descending)

```sql
SELECT * FROM orders
ORDER BY price DESC;
```

---

### 14. Sort by quantity (highest first)

```sql
SELECT * FROM orders
ORDER BY quantity DESC;
```

---

### 15. Sort by city (alphabetical)

```sql
SELECT * FROM orders
ORDER BY city ASC;
```

---

## 🔹 PART 4: LIMIT & OFFSET

### 16. Top 3 most expensive orders

```sql
SELECT * FROM orders
ORDER BY price DESC
LIMIT 3;
```

---

### 17. Bottom 2 cheapest orders

```sql
SELECT * FROM orders
ORDER BY price ASC
LIMIT 2;
```

---

### 18. Second highest price order

```sql
SELECT * FROM orders
ORDER BY price DESC
LIMIT 1 OFFSET 1;
```

---

### 19. 4th and 5th records based on price

```sql
SELECT * FROM orders
ORDER BY price ASC
LIMIT 2 OFFSET 3;
```

---

## 🔹 PART 5: AGGREGATE FUNCTIONS

### 20. Total number of orders

```sql
SELECT COUNT(*) AS total_orders FROM orders;
```

---

### 21. Maximum order price

```sql
SELECT MAX(price) AS max_price FROM orders;
```

---

### 22. Minimum order price

```sql
SELECT MIN(price) AS min_price FROM orders;
```

---

### 23. Average order price

```sql
SELECT AVG(price) AS avg_price FROM orders;
```

---

### 24. Total revenue (sum of prices)

```sql
SELECT SUM(price) AS total_revenue FROM orders;
```

---

## 🔹 PART 6: GROUP BY

### 25. Number of orders per category

```sql
SELECT category, COUNT(*) AS order_count
FROM orders
GROUP BY category;
```

---

### 26. Average price per category

```sql
SELECT category, AVG(price) AS avg_price
FROM orders
GROUP BY category;
```

---

### 27. Total revenue per city

```sql
SELECT city, SUM(price) AS total_revenue
FROM orders
GROUP BY city;
```

---

### 28. Maximum price per category

```sql
SELECT category, MAX(price) AS max_price
FROM orders
GROUP BY category;
```

---

## 🔹 PART 7: HAVING

### 29. Categories with average price > 40,000

```sql
SELECT category, AVG(price) AS avg_price
FROM orders
GROUP BY category
HAVING AVG(price) > 40000;
```

---

### 30. Cities with more than 2 orders

```sql
SELECT city, COUNT(*) AS order_count
FROM orders
GROUP BY city
HAVING COUNT(*) > 2;
```






