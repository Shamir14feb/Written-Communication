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
The INSERT INTO statement is used to insert new records in a table.
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


2. SELECT
- The SELECT statement is used to select data from a database.
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
The following SQL statement selects ALL the columns from the "Customers" table:
![Screenshot](https://github.com/Shamir14feb/Written-Communication/blob/main/Screenshot%20Insert%20Table.png?raw=true)

3. UPDATE
- The UPDATE statement is used to modify the existing records in a table.
<pre>
<b>UPDATE</b> table_name
<b>SET</b> column1 = value1, column2 = value2
<b>WHERE</b> condition;
</pre>

4. DELETE
- The DELETE statement is used to delete existing records in a table.
<pre>
<b>DELETE FROM</b> table_name
<b>WHERE</b> condition;
</pre>
