---
author: amgando

aspects:
  - introduction

category: must-know

standards:
  sql.read-single-table.0: 10
  sql.read-single-table.1: 10
  sql.read-single-table.2: 10

links:

  - '[Control which rows are retrieved](https://pgexercises.com/questions/basic/where.html){documentation}'

---

# Control which rows are retrieved

---
## Content

The `FROM` clause is used to build up a set of candidate rows to read results from. In the most basic examples, "candidate rows" are simply the contents of a table. With more complex queries, joining tables comes into play and allows us to create more interesting candidate rows.

Once we've built up our set of candidate rows, the `WHERE` clause allows us to filter for the rows we're interested in - ie. those with a membercost of more than zero, for example. `WHERE` clauses can also have multiple components combined with boolean logic - it's possible to, for instance, search for facilities with a cost greater than 0 and less than 10.

---
## Practice

How can you produce a list of facilities that charge a fee to members?

`facilities` table

![table](https://i.imgur.com/cUIabdz.png)

target output

![output](https://i.imgur.com/T0UXHH8.png)

???

* select * from facilities where membercost > 0;
* select everything from facilities where membercost is greater than zero;
* select * from table('facilities') where column('membercost') gt 0;
* select * from facilities where membercost gt 0;

---
## Revision

How can you produce a list of facilities that charge a fee to members?

`facilities` table

![table](https://i.imgur.com/cUIabdz.png)

target output

![output](https://i.imgur.com/T0UXHH8.png)

???

* select * from facilities where membercost > 0;
* select everything from facilities where membercost is greater than zero;
* select * from table('facilities') where column('membercost') gt 0;
* select * from facilities where membercost gt 0;
