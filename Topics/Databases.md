# Algorithms
Algorithms are a set of instructions that are followed to solve a problem or achieve a particular outcome. 
In the context of computer science and software engineering, algorithms are often used to manipulate data in various structures to produce a specific result. 
They are fundamental to efficient coding and good software design.

# Table of Content
- [Database Management Systems (DBMS)](#Database-Management-Systems-(DBMS))
  - [Database Management Systems (DBMS)](#Database-Management-Systems-(DBMS))
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

#### Data Abstraction 
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

#### Data Independence 
Data independence means changes to the database structure do not affect the applications that use it. There are two types:
- **Physical Data Independence**: Changes to the physical storage of data do not require changes to the logical schema.
- **Logical Data Independence**: Changes to the logical schema do not affect the application’s ability to access data.

#### Efficient Data Access 
DBMSs use complex algorithms and data structures to quickly retrieve data. For instance, a DBMS might use B-trees for indexing, which can significantly speed up data retrieval. Here’s a simple SQL example that uses an index to speed up queries:
```
CREATE INDEX idx_employee_name ON Employees (Name);
SELECT * FROM Employees WHERE Name = 'John Doe';
```
In this example, the `CREATE INDEX` statement creates an index on the `Name` column of the `Employees` table. This index can significantly speed up the `SELECT` statement that searches for employees by name.

- **Data Integrity and Security**: If data is always accessed through the DBMS, the DBMS can enforce integrity constraints on the data. Also, DBMS provides security to protect data.
- **Data Administration**: When several users share the data, centralizing the administration of data can offer significant improvements.
- **Concurrent Access and Crash Recovery**: DBMS schedules concurrent access to the data in such a manner that only one user can access the same data at a time. Also, DBMS provides crash recovery mechanisms to protect data.
- **Reduced Application Development Time**: DBMS supports many important functions that are common to many applications accessing data stored in the DBMS. This, in conjunction with the high-level interface to the data, facilitates quick development of applications.




#### Code Example
```
void BubbleSort(int[] arr)
{
    int n = arr.Length;
    for (int i = 0; i < n - 1; i++)
        for (int j = 0; j < n - i - 1; j++)
            if (arr[j] > arr[j + 1])
            {
                // swap arr[j] and arr[j+1]
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
}
```
