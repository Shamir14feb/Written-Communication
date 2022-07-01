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
    - Equi join
    - Non-equi join (Theta join) 
2. SQL outer join
    - SQL left join or left outer join
    - SQL right join or right outer join
    - SQL full join or full outer join 
3. SQL cross join
4. SQL self join 


![image](https://user-images.githubusercontent.com/48542354/176902886-e940ffcd-93eb-4418-8138-a549acbe3130.png)


#### SQL Inner Join
 The simplest and most common form of a join is the SQL inner join the default of the SQL join types used in most database management systems. It’s the default SQL join you get when you use the join keyword by itself.

The result of the SQL inner join includes rows from both the tables where the join conditions are met.

![image](https://user-images.githubusercontent.com/48542354/176908477-ef6b8e26-7ed3-48b5-a455-041ad886dd31.png)


Syntax:
<pre>
<b>SELECT</b> ColumnList <b>FROM</b> LeftTable L
<b>INNER JOIN</b>  RightTable R
<b>ON</b> L.Column=R.Column
</pre>

#### Equi Join

An equi join is the most common form of SQL inner join used in practice. If the join contains an equality operator e.g. `=` , then it’s an equi-join. 

#### Theta join (Non-equi join)

In general, this a Theta join used to specify operators or conditions (the ON clause in SQL). In practice, this is a rarely used SQL join types. In most cases, the join will use a non-equality condition e.g. `>`


#### SQL self join
 A SQL Self join is a mechanism of joining a table to itself. You would use a self join when you wanted to create a result set joining records in the table with some other records from the same table.

![image](https://user-images.githubusercontent.com/48542354/176908418-07086c9c-c9e4-401e-b2cf-5bdf01ccf226.png)


#### SQL cross join

A CROSS join returns all rows for all possible combinations of two tables. It generates all the rows from the left table which is then combined with all the rows from the right table. This type of join is also known as a Cartesian product(A*B).

For example, if the left table has 100 rows and the right table has 100 then the cross join result will yield 10,000 rows. 

![image](https://user-images.githubusercontent.com/48542354/176908791-4548e52f-3c32-45c0-bfb0-8764f83b4fa6.png)

#### SQL outer join

On joining tables with a SQL inner join, the output returns only matching rows from both the tables. When using a SQL outer join, not only it will list the matching rows, it will also list the unmatched rows from the other tables. 

![image](https://user-images.githubusercontent.com/48542354/176908936-838daf0a-56f0-4caf-a681-e304b3c03cf4.png)

#### Outer Join
 A SQL outer join, as you might expect by now, will return all the rows in both tables. When rows don’t have a match in one of the tables, the field will display a null value. A full SQL outer join combines the effects of the SQL left joins and SQL right joins. Many databases do not support the implementation of full SQL outer joins
 
 ![image](https://user-images.githubusercontent.com/48542354/176910071-a9904754-cf56-4549-8dfa-4f96151acd72.png)

Syntax:
<pre>
<b>SELECT</b> ColumnList <b>FROM</b> LeftTable L
<b>FULL OUTER JOIN</b>  RightTable R
<b>ON</b> L.Column=R.Column
</pre>

#### Left Outer Join
A SQL left outer join will return all the records from the left table in the join clause, regardless of matching records in the right table. The left SQL outer join includes rows where the condition is met plus all the rows from the table on the left where the condition is not met. Fields from the right table with no match will be displayed as null values. 

![image](https://user-images.githubusercontent.com/48542354/176908974-354e8fb5-5c36-4149-9f25-ddd296622549.png)

Syntax:
<pre>
<b>SELECT</b> ColumnList <b>FROM</b> LeftTable L
<b>LEFT JOIN</b>  RightTable R
<b>ON</b> L.Column=R.Column
<b>WHERE</b> R.Column is <b>NULL</b>
</pre>

#### Right Outer Join
A right outer join will return all the records in the right table in the join clause, regardless of matching records in the left table. Using the right SQL outer join includes all the rows from the table on the right. The right SQL outer join is considered a special case and many databases don’t support right joins. Generally, a SQL right join can be rewritten as a SQL left join by simply changing the order of the tables in the query. In this instance, fields from the left table with no match will display null values 

![image](https://user-images.githubusercontent.com/48542354/176909579-d4136ff3-8dc0-427a-a0a3-e6891fb60142.png)

Syntax:
<pre>
<b>SELECT</b> ColumnList <b>FROM</b> LeftTable L
<b>RIGHT JOIN</b>  RightTable R
<b>ON</b> L.Column=R.Column
<b>WHERE</b> R.Column is <b>NULL</b>
</pre>

### SQL Aggregate Functions

An aggregate function in SQL performs a calculation on multiple values and returns a single value. SQL provides many aggregate functions that include avg, count, sum, min, max, etc. An aggregate function ignores NULL values when it performs the calculation, except for the count function. 

An aggregate function in SQL returns one value after calculating multiple values of a column. We often use aggregate functions with the GROUP BY and HAVING clauses of the SELECT statement.

Various types of SQL aggregate functions are:

- Count()
- Sum()
- Avg()
- Min()
- Max()

### COUNT() Function

The `COUNT()` function returns the number of rows in a database table.

Syntax:
```
COUNT(*)
```
or  
```
COUNT( [ALL|DISTINCT] expression )  
```

### SUM() Function

The `SUM()` function returns the total sum of a numeric column.

Syntax:
```
SUM()  
```
or  
```
SUM( [ALL|DISTINCT] expression )  
```

### AVG() Function

The `AVG()` function calculates the average of a set of values.

Syntax:
```
AVG()
```
or  
```
AVG( [ALL|DISTINCT] expression )  
```

### MIN() Function

The `MIN()` aggregate function returns the lowest value (minimum) in a set of non-NULL values.

Syntax:
```
MIN()  
```
or  
```
MIN( [ALL|DISTINCT] expression )  
```


### MAX() Function

The `MAX()` aggregate function returns the highest value (maximum) in a set of non-NULL values.

Syntax:
```
AVG()  
```
or  
```
AVG( [ALL|DISTINCT] expression )  
```


## References
- [TechTarget](https://www.techtarget.com/searchdatamanagement/definition/SQL)
