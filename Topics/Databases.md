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
These are used to rearrange a given array or list elements according to a comparison operator on the elements.

### Bubble Sort
This is one of the simplest sorting algorithms. It works by repeatedly swapping the adjacent elements if they are in the wrong order. However, it's not suitable for large data sets as its average and worst-case time complexity are both $`O(n^2)`$.

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
