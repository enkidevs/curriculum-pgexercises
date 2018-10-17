---
author: amgando

aspects:
  - introduction

levels:
  - beginner

type: normal

category: must-know

standards:
  sql-new.read-single-table.0: 10

links:

  - '[Retrieve everything from a table](https://pgexercises.com/questions/basic/selectall.html){documentation}'

---

# Retrieve everything from a table

---
## Content

The `SELECT` statement is the basic starting block for queries that read information out of the database. A minimal select statement is generally comprised of `select [some set of columns] from [some table or group of tables]`.

In the most basic case, we want all of the information from the table in question.  Here "table" is a term used for a logical grouping of related information in the database.

The `FROM` section is also easy in the most basic cases - we just need to specify the name of the table from which we want to retrieve the data. When column names are not unique among a group of tables in a database, it's important to use the name of the table to "scope" (meaning to "fully qualify and therefore uniquely identify" ...) the column among all tables.

We can specify that we want all the columns from one or more tables using the shorthand for 'all columns', an asterisk (`*`). We can use this instead of laboriously specifying all the column names in our query.

---
## Practice

How can you retrieve all the information from the `facilities` table?

`facilities` table

![table](https://i.imgur.com/cUIabdz.png)

???

* select * from facilities;
* select everything from facilities;
* select columns from table('facilities');
* select * from table facilities;

---
## Revision

How can you retrieve all the information from the `facilities` table?

`facilities` table

![table](https://i.imgur.com/cUIabdz.png)

???

* select * from facilities;
* select everything from facilities;
* select columns from table('facilities');
* select * from table facilities;

