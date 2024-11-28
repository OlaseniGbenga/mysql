-- select all info from a table
SELECT \* FROM employees;

-- select specific columns info from a table
SELECT first_name, last_name
FROM employees;

-- select all info from a table
SELECT \*
FROM employees
WHERE employee_id =5;

SELECT \*
FROM employees
WHERE employee_id IS NOT NULL
