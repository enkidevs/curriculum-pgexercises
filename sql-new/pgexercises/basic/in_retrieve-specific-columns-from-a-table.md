---
author: amgando

aspects:
  - introduction

category: must-know

standards:
  sql.read-single-table.0: 10
  sql.read-single-table.2: 10

links:

  - '[Retrieve specific columns from a table](https://pgexercises.com/questions/basic/selectspecific.html){documentation}'

---

# Retrieve specific columns from a table

---
## Content

Generally speaking, for queries we care about and will likely reuse, it's considered desirable to specify the names of the columns we want in our queries rather than using `SELECT *`. This is because our application might not be able to cope if more columns get added into the table.

To do this, we specify the columns that we want using a simple comma-delimited list of column names specified in the `SELECT` statement.

The database system will look at the columns available in the `FROM` clause and return the ones we ask for.

---
## Practice

You want to print out a list of all of the facilities and their cost to members. How would you retrieve a list of only facility names and costs?

`facilities` table

![table](https://i.imgur.com/cUIabdz.png)

target output

![output](https://i.imgur.com/Kgo1gf3.png)

???

* select name, membercost from facilities;
* select two columns from facilities;
* select columns('name', 'membercost') from table('facilities');
* select name and membercost from table facilities;

---
## Revision

You want to print out a list of all of the facilities and their cost to members. How would you retrieve a list of only facility names and costs?

`facilities` table

![table](https://i.imgur.com/cUIabdz.png)

target output

![output](https://i.imgur.com/Kgo1gf3.png)

???

* select name, membercost from facilities;
* select two columns from facilities;
* select columns('name', 'membercost') from table('facilities');
* select name and membercost from table facilities;

