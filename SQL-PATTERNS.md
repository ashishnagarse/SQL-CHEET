# SQL Query Patterns

SQL queries follow certain patterns to solve common database problems. Below are some frequently used patterns with examples.

## 📌 1️⃣ Selection and Filtering
Retrieve specific columns and filter records based on conditions.
```sql
SELECT name, age FROM Users WHERE age > 18;
```

## 📌 2️⃣ Sorting Results
Use `ORDER BY` to sort query results.
```sql
SELECT name, age FROM Users ORDER BY age DESC;
```

## 📌 3️⃣ Grouping and Aggregation
Use `GROUP BY` to aggregate data.
```sql
SELECT department, COUNT(*) AS employee_count
FROM Employees
GROUP BY department;
```

## 📌 4️⃣ Subqueries
Use subqueries to fetch data dynamically.
```sql
SELECT name FROM Users WHERE id IN (SELECT user_id FROM Orders);
```

## 📌 5️⃣ Common Table Expressions (CTE)
Use `WITH` for reusable temporary result sets.
```sql
WITH HighSalary AS (
    SELECT name, salary FROM Employees WHERE salary > 50000
)
SELECT * FROM HighSalary;
```

## 📌 6️⃣ Pagination
Limit results for large datasets.
```sql
SELECT * FROM Products ORDER BY price DESC LIMIT 10 OFFSET 20;
```

## 📌 7️⃣ Joins for Combining Data
Join multiple tables to retrieve meaningful data.
```sql
SELECT Customers.name, Orders.amount
FROM Customers
JOIN Orders ON Customers.id = Orders.customer_id;
```

## 📌 8️⃣ Using Indexes for Optimization
Indexes speed up searches in large tables.
```sql
CREATE INDEX idx_users_name ON Users(name);
```

---

🚀 **More SQL patterns will be added!**

