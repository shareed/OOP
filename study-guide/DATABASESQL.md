# Databases

# SQL
**A language designed for interacting with relational database management systems (RDBMS), like MySQL, Oracle, Sqlite etc...**
## Structure
## Relationships
**customers make orders, and orders contain items**
- **One-to-Many**
    - one of the most commonly used type of relationship
    - [Example:](/img/onetoone.png) two tables customers and orders customer may have zero, one or multiple orders. But an order can belong to only one customer
    - Costomers can have **many** orders, order can have only **one** customer
- **One-to-One**
    - [Example:](/img/onetomany.png) two tables customers and addresses, to link the tables you must add a foreign key to the customers table, which has to be a field that refers to the matching record in the Address table
    - customer can have only **one** address and a address can belong to only **one** customer
    - the existence of a relationship can be optional, like having a customer record that has no related address record
- **Many-to-Many**
    - multiple instances on both sides of the relationship
    - [Example](/img/manytomany.png): each order can contain multiple items. And each item can also be in multiple orders
    - this example requires you to create a third table that will link the two tables
    - orders can have many items and items can be in many orders
- **Self Referencing**
    - used when a table needs to have a relationship with itself
    - [Example:](/img/selfreferencing.png) Customers can refer other customers

[More on Relationships]()
## Normalization
- the process of designing your database in such a way that you have no composite columns, little to no redundant data, and that your data dependencies make sense
- There are as many as six or seven stages of normalization, but generally a database is acceptable if it reaches the 3rd stage, called Third Normal Form.
## Syntax
## DDL
## Contraints
- rules that an RDBMS can be made to follow when managing data in a table
- There are 6 common constraints:
    1. Primary Key
    2. Foreign Key
    3. Unique Key
    4. Not Null
    5. Check Constraint
    6. Default Constraint
## DML
## Joins
- When selecting data from multiple tables with relationships
- Cross Joins
- Natural Joins
- Inner Joins
- Left (Outer) Joins
- Right (Outer) Joins
## Unions