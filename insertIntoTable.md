-- inserting values into rows
INSERT INTO employees 
VALUES (1, 'Eugene', 'Krsb', 25.50,'2023-01-02');

-- inserting values into rows
INSERT INTO employees 
VALUES  (2, 'obi', 'mike', 25.50,'2023-01-08'),
        (3, 'Eze', 'shade', 25.50,'2023-01-09'),
        (4, 'mazi', 'house', 25.50,'2023-01-11'),
        (5, 'mide', 'sola', 25.50,'2023-01-03');

-- inserting values into rows at specific column
INSERT INTO employees (employee_id, first_name,last_name)
VALUES (6, 'Gbenga', 'olaseni');

SELECT * FROM employees;