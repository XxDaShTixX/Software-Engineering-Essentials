# Algorithms
Algorithms are a set of instructions that are followed to solve a problem or achieve a particular outcome. 
In the context of computer science and software engineering, algorithms are often used to manipulate data in various structures to produce a specific result. 
They are fundamental to efficient coding and good software design.

# Table of Content
- [Database Management Systems (DBMS)](#database-management-systems-dbms)
  - [Database Management Systems (DBMS)](#database-management-systems-dbms-1)
  - [Relational Databases](#Relational-Databases)
  - [SQL (Structured Query Language)](#SQL)
  - [NoSQL Databases](#NoSQL-Databases)
- [Database Operations](#Database-Operations)
  - [CRUD Operations](#CRUD-Operations)
  - [ACID Properties](#ACID-Properties)
- [Database Design](#Database-Design)
  - [Database Schema](#Database-Schema)
  - [Normalization](#Normalization)
  - [Indexes](#Indexes)
- [Data Processing](#Data-Processing)
  - [ETL (Extract, Transform, Load)](#ETL-(Extract,-Transform,-Load))
- [Data Storage and Retrieval](#Data-Storage-and-Retrieval)
  - [Data Warehousing](#Data-Warehousing)
  - [Distributed Databases](#Distributed-Databases)
- [Database Security](#Database-Security)
  - [Database Security](#Database-Security)
  - [Database Backup and Recovery](#Database-Backup-and-Recovery)
 
## Database Management Systems (DBMS)
The DBMS category covers the systems used for database management. It introduces DBMS and its role, explores relational databases and SQL, and discusses NoSQL databases and their unique use cases. This provides a foundation for understanding various database systems and their applications.

### Database Management Systems (DBMS)
A Database Management System (DBMS) is a software system that enables users to define, create, maintain and control access to the database. It acts as an interface between the user and the database and manages the interaction between them. Here are some key points to understand about DBMS:

#### <ins>Data Abstraction</ins>
Data abstraction refers to the DBMS’s ability to hide the complexities of how data is stored and managed. There are three levels of data abstraction:
- **Physical Level (Internal Level)**: This is the lowest level of data abstraction. It describes how the data is actually stored in the database. It deals with complex low-level data structures, storage allocation, data access paths, and indexes. For instance, it might specify that data is stored in B-trees or hash tables. Users typically don’t interact with this level.
- **Logical Level (Conceptual Level)**: This level comprises information about what data is stored in the database and the relationships among the data. It describes the structure of the whole database for a community of users. It abstracts away the underlying storage and implementation details. For example, in a relational database, the logical level will specify the tables, fields, and relationships between tables.
```
-- Logical Level
CREATE TABLE Employees (
    ID INT PRIMARY KEY,
    Name VARCHAR(50),
    Position VARCHAR(50),
    Department VARCHAR(50)
);
```
In the previous example, the `CREATE TABLE` statement operates at the logical level, defining the structure of the Employees table.
- **View Level (External Level)**: This is the highest level of abstraction and it describes only part of the entire database. The view level provides a user-friendly way of accessing the database as it only displays information that is relevant to a user. It abstracts away the complexities of the physical and logical levels. For example, a user might interact with a view that shows a subset of the data from a table or a join of multiple tables.
```
-- View Level
SELECT Name, Position FROM Employees WHERE Department = 'Sales';
```
In the previous example, the `SELECT` statement operates at the view level, retrieving only the `Name` and `Position` of employees in the ‘Sales’ department.

#### <ins>Data Independence</ins>
Data independence means changes to the database structure do not affect the applications that use it. There are two types:
- **Physical Data Independence**: Changes to the physical storage of data do not require changes to the logical schema.
- **Logical Data Independence**: Changes to the logical schema do not affect the application’s ability to access data.

#### <ins>Efficient Data Access</ins> 
DBMSs use complex algorithms and data structures to quickly retrieve data. For instance, a DBMS might use B-trees for indexing, which can significantly speed up data retrieval. Here’s a simple SQL example that uses an index to speed up queries:
```
CREATE INDEX idx_employee_name ON Employees (Name);
SELECT * FROM Employees WHERE Name = 'John Doe';
```
In the previous example, the `CREATE INDEX` statement creates an index on the `Name` column of the `Employees` table. This index can significantly speed up the `SELECT` statement that searches for employees by name.

#### <ins>Data Integrity and Security</ins> 
DBMSs enforce data integrity through a set of integrity rules that the database must never violate. DBMSs also manage data security by controlling who can access the database and what operations they can perform. Here’s an example of a SQL statement that enforces data integrity:
```
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    ProductID INT REFERENCES Products(ProductID),
    Quantity INT CHECK (Quantity > 0)
);
```
In the previous example, the `REFERENCES` keyword enforces referential integrity (every `ProductID` in the `Orders` table must exist in the `Products` table), and the `CHECK` keyword enforces domain integrity (the Quantity must be greater than 0).

#### <ins>Data Administration</ins> 
DBMSs provide tools for data administration tasks like backup and recovery, data import/export, and performance monitoring and tuning. These tasks are typically performed using the DBMS’s administrative interfaces and are not usually done with code.

#### <ins>Concurrent Access and Crash Recovery</ins> 
DBMSs manage concurrent access to data, ensuring that multiple users can safely access the data at the same time without conflicts. They also provide crash recovery mechanisms to protect data in case of a system failure. These features are built into the DBMS and are not typically controlled with code.

#### <ins>Reduced Application Development Time</ins> 
Since DBMSs provide many common functions needed by applications (like CRUD operations and transaction management), using a DBMS can significantly reduce application development time. For example, instead of writing complex code to read and write data to files, a developer can use simple SQL statements:
```
INSERT INTO Employees (Name, Position) VALUES ('John Doe', 'Software Engineer');
SELECT * FROM Employees WHERE Position = 'Software Engineer';
UPDATE Employees SET Position = 'Senior Software Engineer' WHERE Name = 'John Doe';
DELETE FROM Employees WHERE Name = 'John Doe';
```
In the previous example, these SQL statements perform the basic <ins>CRUD</ins> operations: Create (INSERT), Read (SELECT), Update (UPDATE), and Delete (DELETE).



### Relational Databases
A relational database is a type of database that stores and provides access to data points that are related to one another. Relational databases are based on the relational model, an intuitive, straightforward way of representing data in tables. Here are some key points to understand about relational databases:
- **Tables**: In a relational database, data is organized into one or more tables. Each table is identified by a name (e.g., “Customers” or “Orders”). Tables contain rows (records) and columns (fields).
- **Rows**: Each row in the table represents a unique instance of an object in the table. For example, in a “Customers” table, each row would represent a different customer.
- **Columns**: Each column in the table represents a certain attribute of the object modeled by the table. For example, in a “Customers” table, columns might include “CustomerID”, “Name”, “Address”, etc.
- **Keys**: A key is a field, or combination of fields, in a table that is used to uniquely identify a record in a table. The most common types of keys are the primary key and foreign key.
  - *Primary Key*: A primary key is a column or a set of columns that uniquely identifies each row in the table. A table can have only one primary key.
  - *Foreign Key*: A foreign key is a column or a set of columns used to establish a link between the data in two tables.
- **Relations**: Relations or relationships are established between tables in the database. The most common types of relations are one-to-one, one-to-many, and many-to-many.
- **Normalization**: Normalization is the process of organizing data in a database to avoid duplication and redundancy, and improve data integrity.
- **SQL (Structured Query Language)**: SQL is a programming language used by most relational databases for querying and managing data.



### SQL (Structured Query Language)

#### <ins>Purpose</ins>
SQL is used to perform all types of data operations in a relational database. This includes creating databases and tables, inserting, updating, and deleting data, and querying the database to retrieve data.

#### <ins>SQL Statements</ins> 
SQL is composed of statements, each of which performs a specific task. Some common SQL statements include:
- `SELECT`: Retrieves data from one or more tables.
- `INSERT INTO`: Inserts new data into a table.
- `UPDATE`: Modifies existing data in a table.
- `DELETE`: Removes data from a table.
- `CREATE TABLE`: Creates a new table.
- `DROP TABLE`: Deletes a table.

#### <ins>Querying Data</ins> 
One of the most common uses of SQL is to query data. SQL provides a powerful and flexible way to specify what data you want to retrieve, including filtering, sorting, and aggregating data.

#### <ins>Data Definition Language (DDL)</ins> 
This part of SQL allows you to define and manage database objects. DDL commands include `CREATE`, `ALTER`, and `DROP`.
```
-- Create a new table
CREATE TABLE Customers (
    CustomerID INT PRIMARY KEY,
    Name VARCHAR(50),
    Address VARCHAR(100)
);
```

#### <ins>Data Manipulation Language (DML)</ins> 
This part of SQL is used for managing data within database objects. DML commands include `SELECT`, `INSERT`, `UPDATE`, and `DELETE`.
```
-- Query data from the table
SELECT * FROM Customers WHERE CustomerID = 1;

-- Insert data into the table
INSERT INTO Customers (CustomerID, Name, Address) VALUES (1, 'John Doe', '123 Main St');

-- Update data in the table
UPDATE Customers SET Address = '456 Oak St' WHERE CustomerID = 1;

-- Update data in the table
UPDATE Customers SET Address = '456 Oak St' WHERE CustomerID = 1;
```

#### <ins>Data Control Language (DCL)</ins> 
This part of SQL is used to control access to data stored in a database. DCL commands include `GRANT` and `REVOKE`.
```
GRANT SELECT, INSERT, UPDATE ON my_database.my_table TO 'someuser'@'somehost';
```
In the previous example, the user `someuser` at host `somehost` is given `SELECT`, `INSERT`, and `UPDATE` privileges on `my_table` in `my_database`.

```
REVOKE INSERT ON my_database.my_table FROM 'someuser'@'somehost';
```
In the previous example, the `INSERT` privilege on `my_table` in `my_database` is taken away from the user `someuser` at host somehost.

#### <ins>Joins</ins> 
SQL allows you to combine rows from two or more tables based on a related column. The most common types of joins are `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, and `FULL JOIN`.
- **INNER JOIN**: The `INNER JOIN` keyword selects records that have matching values in both tables.
```
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```

- **LEFT JOIN (or LEFT OUTER JOIN)**: The `LEFT JOIN` keyword returns all records from the left table (table1), and the matched records from the right table (table2). The result is `NULL` on the right side, if there is no match.
```
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID;
```

- **RIGHT JOIN (or RIGHT OUTER JOIN)**: The `RIGHT JOIN` keyword returns all records from the right table (table2), and the matched records from the left table (table1). The result is `NULL` on the left side, when there is no match.
```
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
RIGHT JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```

- **FULL JOIN (or FULL OUTER JOIN)**: The `FULL JOIN` keyword returns all records when there is a match in either left (table1) or right (table2) table records.
```
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
FULL JOIN Orders ON Customers.CustomerID = Orders.CustomerID;

```

In all the previous examples, `Customers` and `Orders` are tables in a database. `CustomerID` is a column present in both tables that is used to match rows between them. Please replace these with your actual table names and column names.




### NoSQL Databases
NoSQL databases are non-relational databases that are designed to scale out across many servers, and they’re optimized for read and write operations. They are a great fit for many modern applications such as mobile, web, and gaming that require flexible, scalable, high-performance, and highly functional databases to provide great user experiences. Here are some key points to understand about NoSQL databases:

#### <ins>NoSQL Database Types</ins>
There are four main types of NoSQL databases - Document databases, Key-Value stores, Wide-Column stores, and Graph databases. Each type is designed to support specific data models and to solve specific problems.

#### <ins>Schema-less</ins>
NoSQL databases are typically schema-less, which means they allow for more flexibility in storing complex data structures.

#### <ins>Scalability</ins>
NoSQL databases are designed to scale out by distributing the data across many servers. This is different from SQL databases, which are typically scaled up by adding more powerful hardware to a single server.

#### <ins>Performance</ins>
NoSQL databases are optimized for specific types of operations and can provide high performance for certain workloads.

#### <ins>CAP Theorem</ins>
According to the CAP theorem, a distributed system can only guarantee two out of three characteristics: Consistency, Availability, and Partition Tolerance. Different types of NoSQL databases make different trade-offs between these characteristics.

#### <ins>Use Cases</ins>
NoSQL databases are a good fit for use cases where data is not structured or schema is changing rapidly, or where horizontal scalability and speed are important.

