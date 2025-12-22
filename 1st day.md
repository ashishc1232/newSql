# MySQL Database Commands

## 1. CREATE DATABASE

### Syntax

```sql
CREATE DATABASE database_name;
```

### Example

```sql
CREATE DATABASE school;
```

### Explanation

* Creates a new database named `school`
* Database is empty (no tables)

---

## 2. CREATE DATABASE IF NOT EXISTS

### Example

```sql
CREATE DATABASE IF NOT EXISTS school;
```

### Explanation

* Prevents error if database already exists
* Good practice in real projects

---

## 3. SHOW DATABASES

### Example

```sql
SHOW DATABASES;
```

### Explanation

* Lists all databases in MySQL server

---

## 4. USE DATABASE

### Example

```sql
USE school;
```

### Explanation

* Selects `school` database
* All table operations will apply here

---

## 5. ALTER DATABASE

In MySQL, `ALTER DATABASE` is mainly used to **change character set and collation**.

### Example: Change Character Set

```sql
ALTER DATABASE school CHARACTER SET utf8mb4;
```

### Explanation

* Changes default character set of database
* `utf8mb4` supports full Unicode

---

### Example: Change Collation

```sql
ALTER DATABASE school COLLATE utf8mb4_general_ci;
```

### Explanation

* Changes sorting and comparison rules

---

## 6. DROP DATABASE

### Syntax

```sql
DROP DATABASE database_name;
```

### Example

```sql
DROP DATABASE school;
```

### Explanation

* Deletes database permanently
* All tables and data are removed
* No undo

---

## 7. DROP DATABASE IF EXISTS

### Example

```sql
DROP DATABASE IF EXISTS school;
```

### Explanation

* Prevents error if database does not exist
* Safer command

---

## 8. Complete Practical Flow (Recommended Teaching Order)

```sql
CREATE DATABASE college;

SHOW DATABASES;

USE college;

ALTER DATABASE college CHARACTER SET utf8mb4;

DROP DATABASE college;
```

---

## Important Rules (Must Remember)

* Database name should be unique
* `DROP DATABASE` deletes everything permanently
* Always use `IF EXISTS` / `IF NOT EXISTS` in production
* `ALTER DATABASE` does not change existing table structure

---




