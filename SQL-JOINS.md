# SQL Joins Explained

SQL Joins are used to combine data from multiple tables based on a related column.

## 📌 Types of Joins

### 1️⃣ INNER JOIN
Returns matching records from both tables.
#### Example:
```sql
SELECT Customers.name, Orders.amount
FROM Customers
INNER JOIN Orders ON Customers.id = Orders.customer_id;
```
**Customers Table:**
| id | name     |
|----|---------|
| 1  | Alice   |
| 2  | Bob     |

**Orders Table:**
| id | customer_id | amount |
|----|------------|--------|
| 1  | 1          | 500    |
| 2  | 2          | 300    |

**Result:**
| name  | amount |
|-------|--------|
| Alice | 500    |
| Bob   | 300    |

### 2️⃣ LEFT JOIN (or LEFT OUTER JOIN)
Returns all records from the left table and matching records from the right table. If no match, NULL is returned.
#### Example:
```sql
SELECT Customers.name, Orders.amount
FROM Customers
LEFT JOIN Orders ON Customers.id = Orders.customer_id;
```
**Result:**
| name  | amount |
|-------|--------|
| Alice | 500    |
| Bob   | 300    |
| Charlie | NULL |

### 3️⃣ RIGHT JOIN (or RIGHT OUTER JOIN)
Returns all records from the right table and matching records from the left table. If no match, NULL is returned.
#### Example:
```sql
SELECT Customers.name, Orders.amount
FROM Customers
RIGHT JOIN Orders ON Customers.id = Orders.customer_id;
```

### 4️⃣ FULL JOIN (or FULL OUTER JOIN)
Returns all records when there is a match in either left or right table. If no match, NULL is returned.
#### Example:
```sql
SELECT Customers.name, Orders.amount
FROM Customers
FULL JOIN Orders ON Customers.id = Orders.customer_id;
```

### 5️⃣ CROSS JOIN
Returns the Cartesian product of both tables (all combinations).
#### Example:
```sql
SELECT Customers.name, Products.product_name
FROM Customers
CROSS JOIN Products;
```
**Customers Table:**
| id | name     |
|----|---------|
| 1  | Alice   |
| 2  | Bob     |

**Products Table:**
| id | product_name |
|----|-------------|
| 1  | Laptop      |
| 2  | Phone       |

**Result:**
| name  | product_name |
|-------|-------------|
| Alice | Laptop      |
| Alice | Phone       |
| Bob   | Laptop      |
| Bob   | Phone       |

### 6️⃣ SELF JOIN
A table joins itself based on a related column.
#### Example:
```sql
SELECT A.name AS Employee, B.name AS Manager
FROM Employees A
JOIN Employees B ON A.manager_id = B.id;
```
**Employees Table:**
| id | name  | manager_id |
|----|-------|------------|
| 1  | Alice | 2          |
| 2  | Bob   | NULL       |

**Result:**
| Employee | Manager |
|----------|---------|
| Alice    | Bob     |

---

🚀 **More SQL Join examples will be added!**
