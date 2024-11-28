-- create db
-- CREATE DATABASE myDB;

-- drop or delete db
-- DROP DATABASE myDB;

-- use db
-- USE myDB

-- ALTER
--   set to read only
-- ALTER DATABASE myDB READ ONLY = 1;

-- DISABLE READ ONLY
-- ALTER DATABASE myDB READ ONLY = 1;

-- create table with rows
-- CREATE TABLE employees (
-- employee_id INT,
-- first_name VARCHAR(50),
-- last_name VARCHAR(50),
-- hourly_pay DECIMAL(5,2),
-- hire_date DATE
-- );

-- select info from table
 SELECT * FROM employees;

-- rename table
-- RENAME TABLE workers TO employees;

-- alter a table
-- ALTER TABLE employees
-- ADD phone_number VARCHAR(15);

-- CHANGE CONLUMN
ALTER TABLE employees
CHANGE COLUMN phone_number email VARCHAR(255);

-- MOVE COLUMN
-- ALTER TABLE employees 
-- MODIFY email VARCHAR(255)
-- AFTER last_name
 
 -- drop column
ALTER TABLE employees 
DROP COLUMN email ;

