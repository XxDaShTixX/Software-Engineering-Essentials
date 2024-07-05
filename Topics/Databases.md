# Algorithms
Algorithms are a set of instructions that are followed to solve a problem or achieve a particular outcome. 
In the context of computer science and software engineering, algorithms are often used to manipulate data in various structures to produce a specific result. 
They are fundamental to efficient coding and good software design.

# Table of Content
- [Database Management Systems (DBMS)](#database-management-systems-dbms)
  - [Database Management Systems (DBMS)](#database-management-systems-dbms-1)
  - [Relational Databases](#Relational-Databases)
  - [SQL](#SQL)
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
The `CREATE TABLE` statement operates at the logical level, defining the structure of the Employees table.
- **View Level (External Level)**: This is the highest level of abstraction and it describes only part of the entire database. The view level provides a user-friendly way of accessing the database as it only displays information that is relevant to a user. It abstracts away the complexities of the physical and logical levels. For example, a user might interact with a view that shows a subset of the data from a table or a join of multiple tables.
```
-- View Level
SELECT Name, Position FROM Employees WHERE Department = 'Sales';
```
The `SELECT` statement operates at the view level, retrieving only the `Name` and `Position` of employees in the ‘Sales’ department.

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
In this example, the `CREATE INDEX` statement creates an index on the `Name` column of the `Employees` table. This index can significantly speed up the `SELECT` statement that searches for employees by name.

#### <ins>Data Integrity and Security</ins> 
DBMSs enforce data integrity through a set of integrity rules that the database must never violate. DBMSs also manage data security by controlling who can access the database and what operations they can perform. Here’s an example of a SQL statement that enforces data integrity:
```
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    ProductID INT REFERENCES Products(ProductID),
    Quantity INT CHECK (Quantity > 0)
);
```
In this example, the `REFERENCES` keyword enforces referential integrity (every `ProductID` in the `Orders` table must exist in the `Products` table), and the `CHECK` keyword enforces domain integrity (the Quantity must be greater than 0).

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
These SQL statements perform the basic <ins>CRUD</ins> operations: Create (INSERT), Read (SELECT), Update (UPDATE), and Delete (DELETE).



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


