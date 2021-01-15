### Database
**A database is a collection of information that is organized so that it can be easily accessed, managed and updated.** 
_____________________
### Relational Database
**A relational database is a type of database. It uses a structure that allows us to identify and access data in relation to another piece of data in the database. Often, data in a relational database is organized into tables.** 
####Tables : Rows and Columns
- Tables can have hundreds, thousands, sometimes even millions of rows of data, these rows are often called records.
- Tables can also have many columns of data. Columns are labeled with a descriptive name (say, age for example) and have a specific data type. 
______________________

### Relational Database Management System
**A relational database management system (RDBMS) is a program that allows you to create, update, and administer a relational database. Most relational database management systems use the SQL language to access the database.** 

#### SQL - Structured Query Language
**SQL (Structured Query Language) is a programming language used to communicate with data stored in a relational database management system. SQL syntax is similar to the English language, which makes it relatively easy to write, read, and interpret.** 
- Many RDBMSs use SQL (and variations of SQL) to access the data in tables. For example, SQLite is a relational database management system. SQLite contains a minimal set of SQL commands (which are the same across all RDBMSs). Other RDBMSs may use other variants.

**Why do we need SQL?**
- Allows users to access data in the relational database management systems.
- Allows users to describe the data.
- Allows users to define the data in a database and manipulate that data.
- Allows to embed within other languages using SQL modules, libraries & pre-compilers.
- Allows users to create and drop databases and tables.
- Allows users to create view, stored procedure, functions in a database.
- Allows users to set permissions on tables, procedures and views.
[SQL Architecture](../img/sqlarchitecture.png)
_______________________
#### Primary Key
- A primary key is a field in a table which uniquely identifies each row/record in a database table. Primary keys must contain unique values. A primary key column cannot have NULL values.
- A table can have only one primary key, which may consist of single or multiple fields. When multiple fields are used as a primary key, they are called a composite key.
- If a table has a primary key defined on any field(s), then you cannot have two records having the same value of that field(s).
- primary key is created while creating the database and the table. The primary key can also be created after the creation of the table
[Create Primary Key](../img/primarykey.png)

#### Foreign Key
- A foreign key is a key used to link two tables together. This is sometimes also called as a referencing key.
- A Foreign Key is a column or a combination of columns whose values match a Primary Key in a different table.
- The relationship between 2 tables matches the Primary Key in one of the tables with a Foreign Key in the second table
[Table](../img/foreignkey.png)
[Once the tables have been created, the foreign key can be created](../img/foreignkey1.png)
____________________

#### SQL Statements
- **DDL** - Data Definition Language - CREATE, ALTER, DROP
- **DML** - Data Manipulation Language - SELECT, INSERT, UPDATE, DELETE
- **DCL** - Data Control Language - GRANT, REVOKE
- **TCL** - Transaction Control Language - SAVEPOINT, ROLLBACK, COMMIT
_____________
##### SELECT Query
**The SQL SELECT statement is used to fetch the data from a database table which returns this data in the form of a result table. These result tables are called result-sets. **
`SELECT column1, column2, columnN FROM table_name;`
**If you want to fetch all the fields available in the field, then you can use the following syntax**
`SELECT * FROM table_name;`
_____________________
##### SQL Where
**The SQL WHERE clause is used to specify a condition while fetching the data from a single table or by joining with multiple tables. If the given condition is satisfied, then only it returns a specific value from the table. You should use the WHERE clause to filter the records and fetching only the necessary records.**
- The [WHERE](../img/where.png) clause is not only used in the SELECT statement, but it is also used in the UPDATE, DELETE statement.
- `SELECT CUSTOMERS.AGE from CUSTOMERS where AGE > 20;`,  retrieve all the names of customers who's age is greater than 20 
___________________________
##### INSERT Query
**The SQL INSERT INTO Statement is used to add new rows of data to a table in the database.** 
[Example](../img/insert.png)
_____________________

###### SQL Joins
**The SQL Joins clause is used to combine records from two or more tables in a database. A JOIN is a means for combining fields from two tables by using values common to each**
[Example](../img/join.png)

**[Different Types Of Joins](../img/joins.png)**
- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- FULL JOIN