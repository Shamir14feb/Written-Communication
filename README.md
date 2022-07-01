# SQL
SQl is a standard language for storing, manipulating and retrieving data in database.

### What is SQL?
- SQL stands for Structured Query Language.
- SQL is used to communicate with a database.

### What Can SQL do?
- Execute queries against a database
- Retrive data from a database
- Insert records in a database
- Update records in a database
- Create new database
- Create new tables in a database

### Syntax help

#### CREATE DATABASE
<pre>
<b>CREATE DATABASE</b> database_name ; 
</pre>
Example
<pre>
<b>CREATE DATABASE</b> testDB;
</pre>
The following SQL statement creates a database called "testDB":


#### USE DATABASE
<pre>
<b>USE</b> database_name 
</pre>
Example
<pre>
<b>USE</b> testDB;
</pre>
The following SQL select testDB database


#### CREATE TABLE
<pre>
<b>CREATE TABLE</b> table_name (column1 datatype, column2 datatype, .......) ;
</pre>
Example
<pre>
<b>CREATE TABLE</b> Persons (
    PersonID int
    LastName varchar(255),
    FirstName varchar(255),
    Address varchar(255),
    City varchar(255)
);
</pre>
The following example creates a table called "Persons" that contains five columns: PersonID, LastName, FirstName, Address, and City:
- The PersonID column is of type int and will hold an integer.
- The LastName, FirstName, Address, and City columns are of type varchar and will hold characters, and the maximum length for these fields is 255 characters.
- The empty "Persons" table will now look like this:
![Screenshot](https://github.com/Shamir14feb/Written-Communication/blob/main/Screenshot%20Create%20Table.png?raw=true)


#### ALTER
- The `ALTER TABLE` statement is used to add, delete, or modify columns in an existing table.

To add a column in a table, use the following syntax
<pre>
<b>ALTER TABLE</b> table_name <b>ADD</b> column_name datatype ; 
</pre>

To delete a column in a table, use the following syntax
<pre>
<b>ALTER TABLE </b> table_name <b>DROP COLUMN</b> column_name;
</pre>

To change the data type of a column in a table, use the following syntax:
<pre>
<b>ALTER TABLE</b> table_name <b>MODIFY COLUMN</b> column_name datatype;
</pre>



#### TRUNCATE
<pre>
<b>TRUNCATE TABLE</b> table_name ; 
</pre>
The TRUNCATE TABLE command deletes the data inside a table, but not the table itself.



#### DROP
<pre>
<b>DROP TABLE</b> table_name
</pre>
The DROP TABLE command deletes a table in the database.



#### RENAME
<pre>
<b>RENAME TABLE</b> table_name <b>TO</b> new_table_name ;
</pre>
**`RENAME TABLE`** offers more flexibility. It allows renaming multiple tables in one statement. This can be useful when replacing a table with a new pre-populated version



#### COMMENT
   ##### Single Line Comments
   - Single line comments start with `--`.
   - Any text between `--` and the end of the line will be ignored (will not be executed).
  ``` 
  --Line1; 
  ```
  
   ##### Multi-Line Comments
   - Any text between `/*` and `*/` will be ignored.
   - Multi-line comments start with `/*` and end with `*/`.
  ``` 
    /* Line1,
       Line2*/ 
  ```



### DLM Commands Syntax

#### INSERT 
The `INSERT INTO` statement is used to insert new records in a table.
1. Specify both the column names and the values to be inserted:
<pre>
<b>INSERT INTO</b> table_name (column1, column2, ....) <b>VALUES</b> (value1, value2, ....);
</pre>

2. If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. Here, the INSERT INTO syntax would be as follows:
<pre>
<b>INSERT INTO</b> table_name <b>VALUES</b> (value1, value2, ....);
</pre>
Example
<pre>
<b>INSERT INTO</b> Persons (PersonId, LastName, FirstName, Address, City) <b>VALUES</b> (1,'Hansen','Ola','Timoteivn 10','Sandnes');
<b>INSERT INTO</b> Persons (PersonId, LastName, FirstName, Address, City) <b>VALUES</b> (2,'Svendson','Tove','Borgvn 23','Sandnes');
<b>INSERT INTO</b> Persons (PersonId, LastName, FirstName, Address, City) <b>VALUES</b> (3,'Pettersen','Kari','Storgt 20','Stavanger');
</pre>


#### SELECT
- The `SELECT` statement is used to select data from a database.
- The data returned is stored in a result table, called the result-set.
<pre>
<b>SELECT</b> column1, column2, ....
<b>FROM</b> table_name;
</pre>
Here, column1, column2, ... are the field names of the table you want to select data from. If you want to select all the fields available in the table, use the following syntax:
<pre>
<b>SELECT * FROM</b> table_name;
</pre>
Example
<pre>
<b>SELECT * FROM</b> Persons;
</pre>
The following SQL statement selects ALL the columns from the "Persons" table:
![Screenshot](https://github.com/Shamir14feb/Written-Communication/blob/main/Screenshot%20Insert%20Table.png?raw=true)

#### UPDATE
- The `UPDATE` statement is used to modify the existing records in a table.
<pre>
<b>UPDATE</b> table_name
<b>SET</b> column1 = value1, column2 = value2
<b>WHERE</b> condition;
</pre>

#### DELETE
- The `DELETE` statement is used to delete existing records in a table.
<pre>
<b>DELETE FROM</b> table_name
<b>WHERE</b> condition;
</pre>

### SQL JOINS
A `JOIN` clause is used to combine rows from two or more tables, based on a related column between them.
A SQL Join is a special form of generating a meaningful data by combining multiple tables relate to each other using a “Key”. Typically, relational tables must be designed with a unique column and this column is used to create relationships with one or more other tables. When you need a result-set that includes related rows from multiple tables, you’ll need to use SQL join on this column 

 The various SQL join types are as follows

   1. SQL inner join
       a. Equi join
       b. Non-equi join (Theta join) 
   2. SQL outer join
       a. SQL left join or left outer join
       b. SQL right join or right outer join
       c. SQL full join or full outer join 
   3. SQL cross join
   4. SQL self join 
