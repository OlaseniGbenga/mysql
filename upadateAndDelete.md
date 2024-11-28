-- update column
UPDATE employees
SET hourly_pay =10.2
WHERE employee_id = 6;

-- update  column to the same value for every instance
UPDATE employees
SET hourly_pay =10.2;

-- delete row always use where clause
DELETE FROM employees
WHERE employee_id = 6;

-- select all info from a table
SELECT * FROM employees;
