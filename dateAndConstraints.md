CREATE TABLE test(
my_date DATE,
my_time TIME,
my_dateTime DATETIME
);

-- INSERTING CURRENT TIME
INSERT INTO test 
VALUES(
CURRENT_DATE(),
CURRENT_TIME(),
NOW()
);

DROP TABLE PRODUCTS;


-- unique constraint --WE CANT INSERT MULTIPLE PRODUCT NAME THAT SRE THE SAME
CREATE TABLE products (
product_id INT,
product_name VARCHAR(25) UNIQUE,
price DECIMAL(4,2)
);

-- adding unique constraint after creating table
ALTER TABLE products 
ADD CONSTRAINT
UNIQUE(product_name);

SELECT * FROM products;

INSERT INTO products
VALUES (100, 'HAMBUGER', 3.99),
(101, 'FRIES', 1.98),
(102, 'SODA',1.00),
(103,'ICE CREAM', 1.49);

-- NOT NULL CONSTRAINT
CREATE TABLE products (
product_id INT,
product_name VARCHAR(25) UNIQUE,
price DECIMAL(4,2) NOT NULL
);

-- NOT NULL CONSTRAINT TO ALREADY CREATED TABLE
ALTER TABLE products 
MODIFY price DECIMAL(4,2) NOT NULL;


-- CHECK CONSTRAINT IS USE TO LIMIT WHAT VALUE CAN BE PLACED IN A COLUMN
CREATE TABLE students(
student_id INT,
first_name VARCHAR(50),
last_name VARCHAR(50),
up_keep DECIMAL(5,2),
CONSTRAINT chk_up_keep CHECK (up_keep >=10.00)
);

-- CHECK CONSTRAIT FOR ALREADY CREATED TABLE
ALTER TABLE employees
ADD CONSTRAINT chk_hourly_pay CHECK(hourly_pay >= 10.00);

-- This should now throw an error because it violates the constraint.
INSERT INTO employees
VALUES (7, "GBENGA", "JOEL", 5.00, "2023-01-07");

-- dro check table
ALTER TABLE employees
DROP  chk_hourly_pay;
-- DEFAULT: WHEN INSERTING A NEW ROW IF WE DO NOT SPECIFY THE VALUE, WE CAN GIVE IT A VALUE BY DEFAULT


SELECT * FROM employees;