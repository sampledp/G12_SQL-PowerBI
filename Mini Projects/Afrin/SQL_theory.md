
## SQL essentials
- SQL abbreviated as Structured Query Language.
- **Database:** A structured set of data held in a computer, typically organized for easy retrieval and manipulation.
- **Table:** A collection of data organized into rows and columns.
- **Column:** Also known as fields or attributes, columns represent the different types of data stored in a table.
- **Row:** A single record in a table, containing data for each column.

## Basic Syntax

- **SELECT:** Specifies the columns that want to retrieve from the table.
- **FROM:** Specifies the table from which want to retrieve the data.
- **ORDER BY:** Arranges the result set in ascending (ASC) or descending (DESC) order based on the specified column(s).

```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1 ASC;
```

### DDL (Data Definition Language)

- DDL deals with the structure and definition of the database objects.
- It includes commands for creating, altering, and dropping database objects like tables, indexes.
```sql
  CREATE TABLE datasheet(
   id INT;
   name VARCHAR(20),
   dept VARCHAR(7),
   address VARCHAR(100)
);
```
### DML (Data Manipulation Language)

- DML deals with the manipulation of data stored in the database.
- It includes commands for inserting, updating, deleting, and retrieving data from database tables.
```sql
INSERT INTO datasheet VALUES
(1,'ANTONY','CSE',12345),
(2,'BARLY','BME',67890),
(3,'CHARLIE','EEE',43667),
(4,'DAISY','ECE',18655),
(5,'DORA','CSE',10945),
(6,'ALAN','EEE',16565),
(7,'ADAM','CSE',10235),
(8,'ARUN','AERO',18655);
```

### DQL (Data Query Language)

- DQL is a subset of SQL that specifically deals with querying and retrieving data from the database.
- It includes only the SELECT statement for retrieving data from one or more tables.
```sql
SELECT * FROM datasheet WHERE dept = 'BME'
```

## Constraints
- Enforce data integrity using constraints such as:
  - **Primary keys**: Ensure uniqueness of each row's primary key value.
  - **Foreign keys**: Establish relationships between tables to maintain referential integrity.
  - **Unique constraints**: Ensure uniqueness of values within a column or set of columns.
  - **Check constraints**: Enforce domain integrity by limiting the values that can be placed in a column.
  ```sql
   CREATE TABLE datasheet (
        id INT PRIMARY KEY,
        name VARCHAR(20),
        dept VARCHAR(7),
        address VARCHAR(100);
  ```
  
## Functions and Aggregates
- Use SQL functions and aggregates for performing calculations and transformations on data.
- Functions can manipulate data values, perform string manipulation, date arithmetic, etc.
- Aggregates perform calculations on sets of values and return a single result.
  ```sql
  SELECT AVG(price) FROM Products
   SELECT MIN(price) FROM Products;
   SELECT MAX(price) FROM Products;
   SELECT COUNT(price) FROM Products;;
  ```

## Views
- Create and manage views, which are virtual tables derived from the results of a SQL query.
- Views can simplify complex queries, provide security by restricting access to certain columns, and abstract underlying table structures.
  ```sql
  CREATE VIEW clg_record AS
  SELECT id, name, dept
  FROM datasheet
  WHERE dept = 'BME';
  ```

## Stored Procedures and Functions
- Utilize stored procedures and functions for encapsulating and executing reusable SQL code.
- Stored procedures are precompiled sets of SQL statements stored in the database.
- Functions are similar to stored procedures but return a value and can be used in SQL statements.
  ```sql
  CREATE PROCEDURE GetEmployeeAddress
      @employee_id INT
  AS
  BEGIN
      SELECT address FROM Employees WHERE id = @employee_id;
  END;
  ```

## Indexes and Performance Optimization
- Create and use indexes to optimize query performance and improve database efficiency.
- Indexes speed up data retrieval by providing quick access paths to rows in database tables.
  ```sql
  CREATE INDEX idx_name ON Customers(name);
  ```

## Transactions and Concurrency Control
- Manage transactions and concurrency control mechanisms to maintain data consistency and integrity in multi-user environments.
- Transactions ensure that groups of operations are executed atomically and either all succeed or fail together.

  ```sql
  BEGIN TRANSACTION;
  UPDATE Products SET price = price * 0.9 WHERE id = 1;
  INSERT INTO Transactions (product_id, amount) VALUES (1, -10);
  COMMIT TRANSACTION;
  ```

## Security
- Understand SQL security principles and mechanisms for controlling access to database objects and data.
- Implement user authentication, authorization, and access control to protect sensitive data.

  ```sql
  CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
  GRANT SELECT ON Customers TO 'username'@'localhost';
  ```

## Advanced SQL Features
- Discover advanced SQL features and techniques for handling complex queries, data manipulation, and performance optimization.
- This includes features such as window functions, common table expressions (CTEs), recursive queries, etc.

  ```sql
  SELECT id, name, dept, address,
         ROW_NUMBER() OVER (PARTITION BY dept ORDER BY name) AS RowNum
  FROM Employees;
  ```

# SQL JOINs

- SQL JOINs are used to combine rows from two or more tables based on a related column between them. 
- Bringing the two tables by same key based on identifier
- There are several types of JOINs:
  
## 1. INNER JOIN
- Inner join returns the rows that have matching values in both tables
- for eg: it could only bring the values from the tables which has same value

```sql
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```

## 2. LEFT JOIN
- LEFT  join matches the data of the first table or with the data in the second table
- If the data is matched, the records are combined, otherwise, NULL is returned

```sql
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.column = table2.column;
```

## 3. RIGHT JOIN 
- RIGHT join matches the data of the second table or  with the data in the first table
```sql
SELECT columns
FROM table1
RIGHT JOIN table2
ON table1.column = table2.column;
```

## 4. FULL OUTER JOIN
- Outer join returns all rows tables either it has match or not

```sql
SELECT columns
FROM table1
FULL OUTER JOIN table2
ON table1.column = table2.column;
```
