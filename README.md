# SQL-Interview-Questions
To Share SQL knowledge and findings

1. What is the difference between DELETE and TRUNCATE?

### DELETE
* Used to delete a row in a table.
* Can rollback
* DML command
* Slower than truncate.

### Truncate
* Used to delete all the rows from a table.
* Cannot rollback.
* DDL command.
* faster.

2. What are the different subsets of SQL?
* DDL - define a database schema
* DML - Manipulation of data.
* DCL - Rights, permissions, and other controls of the DB system.
* TCL - Transaction of DB

3. What do you mean by DBMS? What are its different types?
* A Database Management System (DBMS) is a software application that interacts with the user, applications, and the database itself to capture and analyse data.

4. What do you mean by table and field in SQL?
* Table - a collection of data in an organized manner in the form of rows and columns.
* Field - Column in a table

5. What are joins in SQL?
* There are 4 types,
  1. Inner Join
  2. Full Join
  3. Left Join
  4. Right Join
 
6. What is the difference between the CHAR and VARCHAR2 data types in SQL?
### CHAR 
* used for strings of fixed length.
* Ex - char(10) can only store 10 characters and will not be able to store a string of any other length

### VARCHAR2
* used for character strings of variable length.
* Ex - varchar2(10) can store any length, i.e., 6, 8, 2 in this variable.

7. What is a Primary key?
* Used to uniquely identify evety tuple.

8. What are constraints?
* Constraints are used to specify the limit on the data type of the table. It can be specified while creating or altering the table statement.
 1. NOT NULL - null cannot stored
 2. UNIQUE - all the values in the column are different
 3. CHECK - ensure that all the values in a column satisfy a specific condition.
 4. DEFAULT - set of default values for a column when no value is specified.
 5. INDEX - used to create and retrieve data from the database very quickly.

9. What is the difference between SQL and MySQL?
### SQL
* Structured Query Language.
* Core of relational DB, which is used for accessing and managing the database.

### MySQL
* An open-source relational database management system
* backed by Oracle.

10. What is a Unique Key?
* Uniquely identifies a single row in a table.
* Multiple values allowed per table.
* Null values are allowed.
* Duplicate values are not allowed.

11. What is a Foreign Key?
* Maintain referential integrity by enforcing a link between the data in two tables.
* The foreign key in the child table references the primary key in the parent table.

12. What do you mean by data integrity?
* Defines the Accuracy of data and consistency of data

13. What is the difference between a clustered and a non-clustered index in SQL?
### Clustered Index
* used for easy retrieval of data / faster
* one table can only have one clustered index.

### Non-Clustered Index
* used for easy retrieval of data / Slower
* One table can have many non-clustered indexes.

14. Write a SQL query to display the current date.
* GETDATE()
* Ex - SELECT GETDATE();

15. What are the different types of joins?
* Inner Join - matching values in both tables
* Full Join - either has a match in the left or the right table.
* Left Join - records from the left table, and also those records that satisfy the condition from the right table.
* Right Join - records from the right table, and also those records that satisfy the condition from the left table.








