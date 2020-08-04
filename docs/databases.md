---
id: databases
title: Databases
---

## Introduction to Databases

### What is Data?
**Factual** or **raw data** that can be stored or recorded in some format.
**Ex:** *textual data, numerical data, voice, images, etc.*

### What is Information?
It is a **processed** or **meaningful** data extracted from the raw or factual data.

**Ex:** *News articles, blog posts, playlists, graphs, etc.*

### Difference Between Data & Information

**Analogy:** Consider *pasta is the dish* that you need to cook, thus it can be called as the **information** that you need, and the *ingredients* to prepare pasta can be considered as the **raw data**.

**NOTE:** The difference between data and information depends on the use case or in the context that we require that particular data or information.

### Importance of Data
**Data is all around us**, without it there can be *no research done, you won't be able to get your products delivered to you, college cannot manage the administrative operations, and so on*. So, it becomes very crucial that we store the data in some format, and use that particular data to extract some meaningful information out of it.

### What is Database?
**Collection of related data** that contains real world entities.

**Ex:** *data about students, employees, automobile, agricultural crops, bank a/c, social media profiles, etc.*

### What is Database Management System (DBMS)?
**DBMS** is an application that is used for **storing, retrieving and processing the data**.

**NOTE:** Databases + DBMS = **Database System**

### Drawbacks of Traditional Storage Methods
One can use traditional methods of storing data, *i.e, to use files or spreadsheets*. But there are some drawbacks to it.
- Not feasible to store **large and complex** data
- **Redundant data** (duplicate data) might crop up at multiple locations in the database
- Due to redundancy there can be **inconsistent data** that has to be updated at multiple locations
- To interact with huge database we **need an application to access, modify or update it regularly**.
- **Data security** is another major problem

Here comes database management systems (DBMS) to the rescue, through which we can perform the above operations, and much more than that.

**For ex:**
- Let's assume that you are running a *social club* where you want to store the *data of all the members, and the activities being conducted, and who are all participating it in, and so on*.
- As and when the club grows, you will reach a point where it becomes difficult to maintain the data in a spreadsheet.
- So, at that point you will have to use some DBMS to store the data, and use it.

- The social media platforms such as *Instagram or Twitter* are nothing but an enhanced and a generalized platforms that are similar to these small social clubs or groups.
- And these platforms must use some form of DBMS to store and manage the enormous amount of data that's being generated every day!

### TYPES OF DATABASES
The databases can be categorized into **centralized** and **decentralized databases**.

In centralized database the data is stored at **one place**.

**Ex:** *Library database in your college library may have only one central database system.*

In **decentralized/distributed database** the data is stored at **multiple locations**.

**Ex:** *Torrents or peer-to-peer file sharing system is the best example for distributed databases, where one can download a large file in the form of chunks of data from multiple locations.*

This is much more quicker, efficient, and resolves the overhead of serving the data stored at one single location.

Here are some of the actual database types:

1. **Relational databases:** Stores the data in the form of **rows/tuples** and **columns** in a **table**.

    **Ex:** *MySQL*

2. **NoSQL or Non-Relational databases:** Stores **complex** and **unstructured data** in non-predefined and flexible database schema.

    **Ex:** *MongoDB*

3. **Hierarchical databases:** Stores data in the form of a **tree like structure**.

    **Ex:** *IBM Information Management System (IMS)*

4. **Cloud databases:** It is stored on a **cloud platform and serves different types of databases**, without the need of complete physical systems (*i.e, it uses virtual machines*).

    **Ex:** *Amazon AWS, Google Cloud, DigitalOcean etc.*

### SQL - Structured Query Language:
It is the database language used to **retrieve and manage relational data**, or it is to be used with **relational DBMS (RDBMS)**.

### SQL Vendors or Apps:
1. MySQL
2. Postgres
3. Oracle
4. MariaDB
5. etc.

### NoSQL Databases
Non-relational or NoSQL databases can store **unstructured or complex data**.

**Ex:** *Instagram post that contains the picture, caption, hashtags, comments, etc.*

### Types of NoSQL Databases
1. **Document-oriented database:** Stores data in **JSON-like document**.

    **Ex:** *MongoDB, Apache CouchDB, etc.*

2. **Key-value storage:** Every **key** has a **value** attached to it (*i.e, key-value pairs*).

    **Ex:** *Redis, Riak, etc.*

3. **Graph database:** Stores data in the form of nodes and edges, where **nodes are the entities** and **an edge is the relationship** between the nodes.

    **Ex:** *GraphDB, Neo4j, Grakn, etc*

4. **Wide-Column stores:** Similar to relational databases, but the data is stored in **large columns instead of rows**.

    **Ex:** *Apache Cassandra, ScyllaDB, etc.*

**NOTE:** Each of these database applications comes with some pros and cons, and it has to be implemented according to the use case.

---

## Using SQLite Library
**SQLite is a software library** that provides a **relational database management system**. It is a lightweight version of *MySQL* or other relational DBMS applications.
Python's standard library comes with *PySQLite API* to work with *SQLite database*.

Using SQLite database one can interact with its database without the need of a database server. Thus SQLite is designed to be **serverless, and self-contained** meaning it requires *minimal resources to run*.

**NOTE:** Using SQLite one can **design the prototype of the database or the database schema (structure)** without much hassles, and then easily migrate the database to the full-fledged DBMSs such as *MySQL or PostgreSQL*.

### SQL Fundamentals
Here are some SQL fundamentals that one needs to know before diving into working with SQLite.

#### **Tables:** 
It contains some related data in the form of **rows and columns**.
- a *table* is identified by its **table name**.
- a *column* is called as **data field or column** itself, that defines the data to be stored.
- a *column* will have a **type** in which the data is to be stored.
- a *column* may also have some **constraints** speficied with it.
- a *row* is the actual data, it is known as a **tuple or record**.

#### Data types or Storage class in SQLite:
**NOTE:** SQL data types differ slightly among its vendors, please refer the documentations.

- **TEXT:** stores **characters or string**
- **INTEGER:** stores **whole numbers** (either positive or negative)
- **REAL:** stores **floating point numbers** or which has **decimal values**
- **NULL:** **missing data** or **unkown** values
- **BLOB:** **binary large object**(BLOB) that can store **large amount of data** in binary format

#### Column Constraints:
Constraints are used to specify some rules for the data in a table

- **NOT NULL:** the column cannot have a **NULL (missing)** value
- **PRIMARY KEY:** the column that contains **unique values**, and should **not be NULL**
- **FOREIGN KEY:** is used to **connect to another column in another table**, that column should be of PRIMARY KEY constraint.

#### SQL Query:
It is a **statement** used to **retrieve or store the data** in a database.

#### Transaction:
It can be **single or multiple queries** or operations performed to a database.

#### SQL Commands:
Some reserved keywords that performs a specific operation:

- **CREATE** is used to create a **new database, table,** etc
- **SELECT** is to **select data** from the database
- **INSERT INTO** is used to insert **new records** to a table
- **UPDATE** **modifies** the **existing records** in a table
- **DELETE** statement **deletes** an **existing record** from a table
- **WHERE** clause is used to **specify a condition while querying** data from database
- **ALTER** is used to **modify database** or **tables**
- **DROP** **deletes** a **table** **(THIS ALSO DELETES THE DATA WITHIN THE TABLE)**

**NOTE:** All of the above keywords are not case sensitive, its a **convention to write SQL commands in upper case**.

### Creation of Database & its Connection
The steps to create a database and connect to it:

**1.** Importing **sqlite3** module

sqlite3 is the module of PySQLite Database API.
```python
import sqlite3
```

**2.** Creating a **connection object**

There are two ways to connect to a database

1. using **database filename**:
```python
...
conn = sqlite3.connect('database_name.db')
```

2. use **in memory object** that runs **freshly in the RAM** everytime we run the sqlite python file:
```python
...
conn = sqlite3.connect(':memory:')
```

**NOTE:** This in memory object is useful, as we don't need to edit the file to comment out already created tables, inserted data, or any other query. Thus it can be **used to create a prototype of the database schema** needed, and later we can migrate it to a database file.

Here the **conn** object is assigned with sqlite3's **connect** method by passing the database filename **database_name.db**. If there exists no database file named *database_name.db*, it creates one.

**3.** Commiting the **transactions(changes)**
```python
...
conn.commit()
```
It is important to commit or save the transactions(changes) that are being made to the database.

**4.** **Close** the **connection** object
```python
...
conn.close()
```
**Close the connection** to make sure the **committed changes are not lost**, or it might run into some errors.

Here's an example of **employee database**, create a python file named *employee.py* and write the following code in it:
```python
import sqlite3

# connect to the database employee.db
conn = sqlite3.connect('employee.db')

# commit & close the connection
conn.commit()
conn.close()
```

Now run this python program, and it creates a database file named *employee.db* in the current directory.
```bash
$python employee.py
```
**NOTE:** It is important to **commit the transactions and close the connection**, if not it may not save the changes, and run into some errors.

### Creation of Tables and Inserting Values

**NOTE:** You can use the same old **employee.py** python file.

**1.** create a **cusor object** is used to traverse the tuples in the database, acting like a pointer.
```python
...
cur = conn.cursor()
...
```

**2.** Using SQL's **CREATE** statement create a **table**
```python
...
cur.execute("""CREATE TABLE table_name(
                column1 type constraint,
                column2 type constraint,
            ...
            )""")
...
```
- cursor object **cur** is used as a **pointer to perform some operation**, be it while creating anything new or on existing data.
- **"execute"** method of the cursor object is used to **execute an SQL statement**.
- Inside the parentheses **triple quotes("""...""")** is used span a single SQL statement or query into **multiple lines**.
- **"CREATE TABLE table_name"** creates a table with the **table_name** that we provide.
- **"column type constraints"** creates the specified **data field or column**, with it's **data type**, and with some **rules or constraints**.

Here is an example of the **employees table:**
```python
...
cur = conn.cursor()

cur.execute("""CREATE TABLE employees(
                first_name text NOT NULL,
                last_name text NOT NULL,
                emp_id text PRIMARY KEY,
                salary integer
            )""")
...
```

### Inserting Data into Tables
The query to insert values as the records of the table is:
```python
...
cur.execute("INSERT INTO table_name VALUES('value1', value2, ...)
...
```

Here is an example to **insert data** into **employees table**:
```python
...
cur.execute("INSERT INTO employees VALUES('John', 'Frusciante', 'E101', 74000)")
cur.execute("INSERT INTO employees VALUES('Chad', 'Smith', 'E102', 62000)")
cur.execute("INSERT INTO employees VALUES('Robert', 'Plant', 'E103', 86000)")
...
```
In here, **three records** will be inserted into the **employees table**.

### To Fetch and Display the Records
We use **SELECT** command to select a **single or multiple records** from the table:
```python
...
cur.execute("SELECT * FROM table_name")
print(cur.fetchall())
...
```
- **asterix(\*)** is used to **traverse through all the records** from the table
- **fetchall()** method returns a list of **all the selected records** from the table
- **fetchone()** fetches a **single record** pointed by the cursor
- **fetchmany(size)** accepts **size** as parameter that returns **number of specified records**

Example for using **SELECT** command in **employees table**
```python
...
cur.execute("SELECT * FROM employees")
print(cur.fetchmany(2))
```
In here, it fetches only **first two records**.

### To Update Existing Records
**UPDATE** statement uses a **SET** command, and **WHERE** clause to **identify the specify record** to be updated or modified, and then **set the new value**.
```python
...
cur.execute("UPDATE table_name SET column_name='new_value' WHERE column_name='row_identifier'")
...
```
- **SET** sets the record selected to the **new_value**
- **WHERE** clause is used to identify the record by a constraint
- the constraint to identify a record is by using **an existing unique value of a column as the row_identifier**.

Example for **updating** the **salary** of the record that has the data **E101**:
```python
...
cur.execute("UPDATE employees SET salary=94000 WHERE emp_id='E103'")
...
```

### To Delete an Existing Record
We use the same **WHERE** clause to **identify a record to be deleted**.
```python
...
cur.execute("DELETE FROM table_name WHERE column_name='row_identifier'")
...
```
Here we are using the same way of setting the constraint for the WHERE clause by using an **existing unique value as row_identifier**.

Example to **delete** the employee record having **emp_id 'E102'**:
```python
...
cur.execute("DELETE FROM employees WHERE emp_id='E102'")
...
```

### PRIMARY KEY Constraint
It is a **rule or constraint** used on a column to only insert the **unique values** into that particular column, **without any missing values** (*i.e, NULL values*).

```python
...
cur.execute("""CREATE TABLE table_name (
                column1 type PRIMARY KEY,
                ...
                ...
            )""")
...
```

Here is an example of **employees table** with **primary key constraint**:
```python
...
cur.execute("""CREATE TABLE employees (
                ...
                emp_id text PRIMARY KEY,
                ...
            )""")
...
```
In here only the **emp_id column** is of **PRIMARY KEY constraint**.

### FOREIGN KEY Constraint
A **FOREIGN KEY constraint** is used to **connect to another table by linking its PRIMARY KEY constraint column**. This is one way of linking or connecting two tables in relational databases.

```python
...
cur.execute("""CREATE TABLE table_name (
                ...
                column_n type NOT NULL,
                FOREIGN KEY (column_n)
                    REFERENCES another_table_name (column_n)
                ...
            """)
...
```
Here we are setting **column_n** to be *NOT NULL*,
- this **column_n** is the same column from another table
- In the next line we are using **FOREIGN KEY** constraint on **column_n**
- and then referring it to the same column that is present in **another_table_name** using **REFERENCES** keyword.
- So, the **column_n** in **table_name** should contain one of the **same unique values** stored in **column_n** of **another_table_name**

As an example we'll create a new table named **emp_department**:
```python
...
cur.excute("""CREATE TABLE emp_department (
                dept_name text NOT NULL,
                designation text NOT NULL,
                emp_id text NOT NULL,
                FOREIGN KEY (emp_id)
                    REFERENCES employees (emp_id)
            )""")
...
```
In here we have the column **emp_id** which is the same column that is in **employees** table as well.


### Employee Database Python Program
Here is the full program where we'll create two tables, insert values, update, and delete some records.
- We'll use python's **functions for these queries** to be performed in an organized way.
- We'll also be using **context managers (i.e, with)**, which **handles the opening and closing of database connections** or any other resources, without running into errors.
- **Placeholders(?)** are used to **assign or pass values** into the table through the queries.

```python
import sqlite3

## connection object to connect to the database 'employee.db'
conn = sqlite3.connect('employee.db')

## create a cursor object to point and execute a query in the database
cur = conn.cursor()

## with context manager to commit the transactions &
## to manage closing of the database connection
with conn:
## create employees table with the columns:
## first_name, last_name, emp_id & salary
   cur.execute("""CREATE TABLE employees (
                    first_name text NOT NULL,
                    last_name text NOT NULL,
                    emp_id text PRIMARY KEY,
                    salary integer NOT NULL
                )""")

with conn:
## create emp_department table with the columns:
## dept_name, designation & emp_id
   cur.execute("""CREATE TABLE emp_department (
                    dept_name text NOT NULL,
                    designation text NOT NULL,
                    emp_id text NOT NULL,
                    FOREIGN KEY (emp_id)
                        REFERENCES employees (emp_id)
                )""")

## a function to insert data into employees table &
## passing data through tuple "emp" as a parameter
def insert_into_employees(emp):
    with conn:
        ## using ? as a placeholder to pass the data from the parameter "emp"
        cur.execute("INSERT INTO employees VALUES(?, ?, ?, ?)", (emp))

## a function to insert data into emp_department table
## passing data through tuple "emp_dept" as a parameter
def insert_into_emp_department(emp_dept):
    with conn:
        cur.execute("INSERT INTO emp_department VALUES(?, ?, ?)", (emp_dept))

## a function to update a particular record in employees table
## passing the data to be updated through the dictionary "update_sal" as a parameter
def update_salary_employees(update_sal):
    with conn:
        ## using key-value pairs for assigning the data to its corresponding column
        ## "salary" being the column name is assigned with the key "sal", in turn using "sal" we assign the new value
        ## {...'sal':update_sal['e_sal']} here, sal is the key & update_sal['e_sal'] is the new value
        cur.execute("UPDATE employees SET salary=:sal WHERE emp_id=:id", {'id':update_sal['e_id'], 'sal':update_sal['e_sal']})

## a function to delete a record from employees table
def del_record_employees(del_emp):
    with conn:
        ## using the same key-value pair way of assigning the data to its corresponding columns
        ## since "emp_id" is the column, "id" is assigned to it as the key,
        ## and inside the {'id': del_emp}, del_emp is the value
        cur.execute("DELETE FROM employees WHERE emp_id=:id", {'id': del_emp})

## a function to display all the records of a table
def disp_all_records(table_name):
    with conn:
        cur.execute("SELECT * FROM " + table_name)
        print(cur.fetchall())

## passing data to be inserted into employees table
## datafields order: ('fist_name', 'last_name', 'emp_id', salary)
emp_john = ('John', 'Frusciante', 'E101', 74000)
emp_chad = ('Chad', 'Smith', 'E102', 62000)
emp_robert = ('Robert', 'Plant', 'E103', 86000)

insert_into_employees(emp_john)
insert_into_employees(emp_chad)
insert_into_employees(emp_robert)

## passing data to be inserted into emp_department table
## datafields order: ('dept_name', 'designation', 'emp_id')
dept_john = ('String Instruments', 'Guitarist', 'E101')
dept_chad = ('Percussion', 'Drummer', 'E102')
dept_robert = ('Vocals', 'Vocalist', 'E103')

insert_into_emp_department(dept_john)
insert_into_emp_department(dept_chad)
insert_into_emp_department(dept_robert)

## passing the salary to be updated using a dictionary to update it
up_sal_john = {'e_id': 'E101', 'e_sal': 82000}
update_salary_employees(up_sal_john)


## passing an emp_id as an arugment to delete that particular record
del_record_employees('E102')

## call disp_all_records function by passing table_name
## as argument to fetch & display records.
disp_all_records("employees")
disp_all_records("emp_department")
```

**NOTE:** These are the basic operations, and there are many ways of writing these transactions or queries in Python or any other language.

### Using sqlite3 CLI
**SQLite** has its own **interactive session** through which one can interact with the databases created using SQLite. Use the following command at the terminal:
```bash
$sqlite3
```

1. To **open a database** file:
```bash
sqlite> .open database_name.db
```

2. To view the database **schema**:
```bash
sqlite> .schema table_name
```

3. To display all the **tables** in the database:
```bash
sqlite> .tables
```

4. To quit or **exit**:
```bash
sqlite> .quit
```

5. To show all the **sqlite3 commands**:
```bash
sqlite> .help
```

6. For more information about **sqlite3 CLI**, read the **man pages**:
```bash
$man sqlite3
```

### For More Info
Since these are the **basic operations** that are in any **database API**, there is more to know about SQLite or SQL in general.

For more info about SQLite CLI - **[click here](https://www.sqlitetutorial.net/sqlite-commands/)**

You can always look into SQLite's documentation for much more about it - **[click here](https://www.sqlitetutorial.net/)**

