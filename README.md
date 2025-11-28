# ODS-QA
ODS QA
WITH recent_orders AS (
    SELECT order_id, customer_id, order_date
    FROM orders
    WHERE order_date > '2025-01-01'
)
SELECT *
FROM recent_orders;


SELECT name
FROM employees
WHERE department_id = (SELECT department_id FROM departments WHERE name = 'Sales');



test cases
