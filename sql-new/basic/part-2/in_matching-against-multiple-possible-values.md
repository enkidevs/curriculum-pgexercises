---
author: amgando

aspects:
  - introduction

category: must-know

standards:
  sql.read-single-table.0: 10
  sql.read-single-table.1: 10

links:

  - '[Matching against multiple possible values](https://pgexercises.com/questions/basic/where4.html){documentation}'

---

# Matching against multiple possible values

---
## Content

We can match against multiple possible values using a `WHERE` clause that looks like `where facid = 1 or facid = 5`. An alternative that is easier with large numbers of possible matches is the `IN` operator. The `IN` operator takes a list of possible values, and matches them against one field that we're interested in. If one of the values matches, the where clause is true for that row, and the row is returned.

The `IN` operator is a good early demonstrator of the elegance of the relational model. The argument it takes is not just a list of values - it's actually a table with a single column. Since queries also return tables, if you create a query that returns a single column, you can feed those results into an `IN` operator.

This is functionally equivalent to just selecting all the rows, but considers our ability to feed the results of one query into another. The inner query is called a "subquery".

---
## Practice

How can you retrieve the details of facilities with ID 1 and 5? Try to do it without using the `OR` operator.

`facilities` table

![table](https://i.imgur.com/cUIabdz.png)

target output

![output](https://i.imgur.com/BlUCtLN.png)

???

* select * from facilities where facid in (1,5);
* select everything from facilities where facid in (1,5);
* select * from facilities where facid in('1','5');
* select * from facilities where facid in 1 and 5;

---
## Revision

How can you retrieve the details of facilities with ID 1 and 5? Try to do it without using the `OR` operator.

`facilities` table

![table](https://i.imgur.com/cUIabdz.png)

target output

![output](https://i.imgur.com/BlUCtLN.png)

???

* select * from facilities where facid in (1,5);
* select everything from facilities where facid in (1,5);
* select * from facilities where facid in('1','5');
* select * from facilities where facid in 1 and 5;

