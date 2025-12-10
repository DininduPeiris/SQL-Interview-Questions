# SQL-Interview-Questions
To Share SQL knowledge and findings

Video link - https://www.youtube.com/watch?v=-WEpWH1NHGU

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

16. What do you mean by Denormalization?
* refers to a technique that is used to access data from higher to  lower forms of a database.
* increase the performance
* introduce data redundancy
* combine data from various tables into a single table.

17. What are Entities and Relationships?
* An Entity is any object, person, place, event, or concept that you want to store information about in a database.
* A Relationship describes how two entities are connected.

18. What is an Index?
* Performance tuning method
* Allows faster retrieval of records from the table
* Creates an entry for each value.

19. Explain different types of index.
### Unique Index
* does not allow duplicate values

### Clustered Index
* reorders the physical order of the table and searches based on the basis of key values.
* Only one clustered index per table.

### Non-Clustered Index
* does not alter the physical order of the table and maintains a logical order of the data.
* Each table can have many non-clustered indexes.

20. What is Normalization, and what are the advantages of it?
* process of organizing data to avoid duplication and redundancy.
### Advantages
* Better DB organization
* More tables with smaller rows.
* Efficient data access
* Greater flexibility of queries.
* Quickly find the information
* Easier to implement security
* Allows easy modification.
* Reduce duplicating data.
* Compact database.
* ensure consistent data after modification

21. What is the difference between DROP and Truncate commands?
### DROP
* removes a table
* cannot rollback
* DROP TABLE table_name;

### TRUNCATE
* removes all rows of the table.
* cannot rollback
* TRUNCATE TABLE table_name;

22. Explain the different types of Normalization.
<img width="1036" height="753" alt="image" src="https://github.com/user-attachments/assets/5c4e5905-3b35-4e22-aa2f-ddc96ef9e581" />

<img width="1188" height="816" alt="image" src="https://github.com/user-attachments/assets/c317ad8c-6baa-405c-af90-81f38dcde781" />

### 1 NF  
* Each table cell should have a single value. So, basically, all the records must be unique.
<img width="1135" height="640" alt="image" src="https://github.com/user-attachments/assets/3042c5dc-7ba8-4171-a348-16bddfd57f8b" />

### 2 NF 
* Database should be 1NF and should also have a single-column primary key.
<img width="1067" height="552" alt="image" src="https://github.com/user-attachments/assets/1a94fcd9-6028-4c6f-a904-087e8d5e6b8a" />

### 3 NF
* The database should be in 2NF and must not have any transitive functional dependencies.
<img width="1182" height="492" alt="image" src="https://github.com/user-attachments/assets/0b401c33-5161-4953-91e1-89d70e5213d4" />

### BCNF
* If your database is in 3rd Normal Form, there would be some scenarios where anomalies would be present if you have more than one candidate key.
* Then BCNF comes into role, where you divide your tables further so that there would be only one candidate key present.
* Candidate Key - A candidate key is any attribute or set of attributes that can uniquely identify a record in a table.

23. What is the ACID property in a database?
* A - Atomicity - A transaction must be treated as a single, indivisible unit.
* C - Consistency - A transaction must bring the database from one valid state to another valid state,
* I - Isolation - Concurrency control - Each transaction must run as if it is the only transaction in the system. Transactions should not interfere with each other’s intermediate states.
* D - Durability - Once a transaction is committed, its data must be permanently saved—even if the system crashes immediately afterward.

24. What do you mean by "Trigger" in SQL?
* Triggers in SQL are a special type of stored procedure that are defined to execute automatically in place or after data modifications. It allows you to execute a batch of code when an insert, update, or any other query is executed against a specific table.
* 6 types
  1. BEFORE INSERT
  2. AFTER INSERT
  3. BEFORE UPDATE
  4. AFTER UPDATE
  5. BEFORE DELETE
  6. AFTER DELETE

25. To count the number of records in a table
* SELECT COUNT(*) FROM table1

26. Write a SQL query to find the names of the employees that begin with 'A'?
* SELECT * FROM employee WHERE empName LIKE 'A%'

27. End with 'A'
* SELECT * FROM employee WHERE empName LIKE '%A'

28. Write a SQL query to get the third-highest salary of an employee from employee_table?
* SELECT * FROM employee_table ORDER BY salary DESC LIMIT 2,1

29. What is the difference between 'BETWEEN' and 'IN' condition operators?
### BETWEEN
* used to display rows based on a range of values in a row.
* SELECT * FROM students WHERE roll_no BETWEEN 10 AND 50

### IN
* Used to check for values contained in a specific set of values.
* SELECT * FROM students WHERE roll_no IN (8, 15, 11);

30. Why are SQL functions used?
* To perform some calculations
* To modify individual data items
* To manipulate the output
* To format dates and numbers
* To convert the data types

31. What is the difference between the 'HAVING' clause and the 'WHERE' clause?
### HAVING
* Filters groups after the GROUP BY and aggregation have been applied.
* Works On: Aggregate functions, Grouped results

```sql
SELECT department, COUNT(*) AS total
FROM employees
GROUP BY department
HAVING COUNT(*) > 10;   -- filters groups after aggregation
```

### WHERE
* Filters rows before grouping or aggregation.
* Works On: Individual rows, Non-aggregated columns
* Cannot use: Aggregate functions (SUM, COUNT, AVG, MAX, MIN)

```sql
SELECT department, COUNT(*)
FROM employees
WHERE salary > 50000   -- filters rows before grouping
GROUP BY department;
```

32. How can you select unique records from a table?
* SELECT DISTINCT studentID FROM student;

33. What is a View?
* A view is a saved SQL query that behaves like a table. It provides a predefined way to look at data without storing duplicate data.

```sql
CREATE VIEW view_name AS
SELECT column1, column2
FROM table_name
WHERE condition;
```

34. What is a stored procedure?
* A stored procedure is a named database object that contains one or more SQL statements and is stored on the database server. It is executed as a single unit, often with input/output parameters. Stored procedures enhance performance, security, and maintainability.

```sql
CREATE PROCEDURE GetHighSalaryEmployees(IN minSalary INT)
BEGIN
    SELECT name, salary
    FROM employees
    WHERE salary > minSalary;
END;

```

```sql
CALL GetHighSalaryEmployees(50000);
```








