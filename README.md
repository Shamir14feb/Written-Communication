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

1. CREATE DATABASE
<pre>
<b>CREATE DATABASE</b> database_name ; 
</pre>
Example
<pre>
<b>CREATE DATABASE</b> testDB;
</pre>
The following SQL statement creates a database called "testDB":


2. USE DATABASE
<pre>
<b>USE</b> database_name 
</pre>
Example
<pre>
<b>USE</b> testDB;
</pre>
The following SQL select testDB database


3. CREATE TABLE
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


4. ALTER
<pre>
<b>ALTER TABLE</b> table_name <b>ADD</b> column_name datatype ; 
</pre>

5. TRUNCATE
<pre>
<b>TRUNCATE TABLE</b> table_name ; 
</pre>

6. DROP
<pre>
<b>DROP TABLE</b> table_name
</pre>

7. RENAME
<pre>
<b>RENAME TABLE</b> table_name <b>TO</b> new_table_name ;
</pre>

8. COMMENT
   - Single Line Comments
  ``` 
  --Line1; 
  ```
   - Multi-Line Comments
  ``` 
    /* Line1,
       Line2*/ 
  ```

###DLM Commands Syntax

1. INSERT 
<pre>
<b>INSERT INTO</b> table_name (column1, column2, ....) <b>VALUES</b> (value1, value2, ....);
</pre>

2. SELECT
<pre>
<b>SELECT</b> column1, column2, ....
<b>FROM</b> table_name;
</pre>

3. UPDATE
<pre>
<b>UPDATE</b> table_name
<b>SET</b> column1 = value1, column2 = value2
<b>WHERE</b> condition;
</pre>

4. DELETE
<pre>
<b>DELETE FROM</b> table_name
<b>WHERE</b> condition;
</pre>
