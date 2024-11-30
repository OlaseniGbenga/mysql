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