# SQL Joins Explained

SQL Joins are used to combine data from multiple tables based on a related column.

## 📌 Types of Joins

### 1️⃣ INNER JOIN
Returns matching records from both tables.
```sql
SELECT Customers.name, Orders.amount
FROM Customers
INNER JOIN Orders ON Customers.id = Orders.customer_id;
```

### 2️⃣ LEFT JOIN (or LEFT OUTER JOIN)
Returns all records from the left table and matching records from the right table. If no match, NULL is returned.
```sql
SELECT Customers.name, Orders.amount
FROM Customers
LEFT JOIN Orders ON Customers.id = Orders.customer_id;
```

### 3️⃣ RIGHT JOIN (or RIGHT OUTER JOIN)
Returns all records from the right table and matching records from the left table. If no match, NULL is returned.
```sql
SELECT Customers.name, Orders.amount
FROM Customers
RIGHT JOIN Orders ON Customers.id = Orders.customer_id;
```

### 4️⃣ FULL JOIN (or FULL OUTER JOIN)
Returns all records when there is a match in either left or right table. If no match, NULL is returned.
```sql
SELECT Customers.name, Orders.amount
FROM Customers
FULL JOIN Orders ON Customers.id = Orders.customer_id;
```

### 5️⃣ CROSS JOIN
Returns the Cartesian product of both tables (all combinations).
```sql
SELECT Customers.name, Products.product_name
FROM Customers
CROSS JOIN Products;
```

### 6️⃣ SELF JOIN
A table joins itself based on a related column.
```sql
SELECT A.name AS Employee, B.name AS Manager
FROM Employees A
JOIN Employees B ON A.manager_id = B.id;
```

---

🚀 **More SQL Join examples will be added!**

