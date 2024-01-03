 <h1>Here is a list what we did throughout the fall 2023 semester </h1>

# 1. AND | OR

```sql
SELECT * FROM employees
WHERE department = 'HR' AND salary > 50000;

```

# 2. ALTER TABLE

```sql
ALTER TABLE customers
ADD COLUMN phone_number VARCHAR(15);

```

# 3. AS (alias)

```sql
SELECT first_name AS "First Name", last_name AS "Last Name"
FROM employees;

```

# 4. BETWEEN

```sql
SELECT * FROM products
WHERE price BETWEEN 10 AND 50;

```

# 5. CREATE DATABASE

```sql
CREATE DATABASE new_database;

```

# 6. CREATE TABLE

```sql
CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    salary DECIMAL(10, 2)
);

```

# 7. CREATE INDEX

```sql
CREATE INDEX idx_employee_id ON employees(employee_id);

```

# 8. CREATE VIEW

```sql
CREATE VIEW high_salaries AS
SELECT * FROM employees WHERE salary > 80000;

```

# 9. DELETE

```sql
DELETE FROM customers
WHERE last_purchase_date < '2023-01-01';

```

# 10. GRANT

```sql
GRANT SELECT, INSERT ON employees TO hr_user;

```

# 11. REVOKE

```sql
REVOKE INSERT ON employees FROM hr_user;

```

# 12. COMMIT

```sql
COMMIT;

```

# 13. ROLLBACK

```sql
ROLLBACK;

```

# 14. SAVEPOINT

```sql
SAVEPOINT sp1;

```

# 15. DROP DATABASE

```sql
DROP DATABASE old_database;

```

# 16. DROP INDEX

```sql
DROP INDEX idx_employee_id ON employees;

```

# 17. DROP TABLE

```sql
DROP TABLE obsolete_table;

```

# 18. EXISTS

```sql
SELECT * FROM orders
WHERE EXISTS (SELECT 1 FROM customers WHERE customers.customer_id = orders.customer_id);

```

# 19. GROUP BY

```sql
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department;

```

# 20. HAVING

```sql
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department
HAVING AVG(salary) > 60000;

```

# 21. IN

```sql
SELECT * FROM products
WHERE category IN ('Electronics', 'Clothing');

```

# 22. INSERT INTO

```sql
INSERT INTO employees (first_name, last_name, salary)
VALUES ('John', 'Doe', 60000);

```

# 23. INNER JOIN

```sql
SELECT employees.first_name, departments.department_name
FROM employees
INNER JOIN departments ON employees.department_id = departments.department_id;

```

# 24. LEFT JOIN

```sql
SELECT customers.customer_id, orders.order_id
FROM customers
LEFT JOIN orders ON customers.customer_id = orders.customer_id;

```

# 25. RIGHT JOIN

```sql
SELECT customers.customer_id, orders.order_id
FROM customers
RIGHT JOIN orders ON customers.customer_id = orders.customer_id;

```

# 26. FULL JOIN

```sql
SELECT customers.customer_id, orders.order_id
FROM customers
FULL JOIN orders ON customers.customer_id = orders.customer_id;

```

# 27. LIKE

```sql
SELECT * FROM products
WHERE product_name LIKE 'Laptop%';

```

# 28. ORDER BY

```sql
SELECT * FROM employees
ORDER BY last_name ASC, first_name DESC;

```

# 29. SELECT

```sql
SELECT first_name, last_name FROM employees;

```

# 30. SELECT \*

```sql
SELECT * FROM employees;

```

# 31. SELECT DISTINCT

```sql
SELECT DISTINCT department FROM employees;

```

# 32. SELECT INTO

```sql
SELECT first_name, last_name INTO new_employees
FROM employees WHERE salary > 70000;

```

# 33. SELECT TOP

```sql
SELECT TOP 5 * FROM products
ORDER BY price DESC;

```

# 34. TRUNCATE TABLE

```sql
TRUNCATE TABLE temporary_data;

```

# 35. UNION

```sql
SELECT customer_id, order_date FROM orders
UNION
SELECT customer_id, registration_date FROM customers;

```

# 36. UNION ALL

```sql
SELECT customer_id, order_date FROM orders
UNION ALL
SELECT customer_id, registration_date FROM customers;

```

# 37. UPDATE

```sql
UPDATE employees
SET salary = salary * 1.1
WHERE department = 'Engineering';

```

# 38. WHERE

```sql
SELECT * FROM products
WHERE category = 'Electronics';

```
