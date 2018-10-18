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
  sql-new.read-single-table.1: 10
  sql-new.read-single-table.2: 10

links:

  - '[Combining results from multiple queries](https://pgexercises.com/questions/basic/union.html){documentation}'

---

# Combining results from multiple queries

---
## Content

The `UNION` operator does what you might expect: combines the results of two SQL queries into a single table. The caveat is that both results from the two queries must have the same number of columns and compatible data types.

`UNION` removes duplicate rows, while `UNION ALL` does not. Use `UNION ALL` by default, unless you care about duplicate results.

---
## Practice

You, for some reason, want a combined list of all surnames and all facility names. Yes, this is a contrived example :-). Produce that list!

`members` table

https://i.imgur.com/BkIONKX.png

`facilities` table

https://i.imgur.com/cUIabdz.png

target output

https://i.imgur.com/QHPpyvL.png

???

* select surname from members union select name from facilities;
* select surname from members and select name from facilities;
* select members('surname') union select facilities('name');
* select surname from members as well as name from facilities;

---
## Revision

You, for some reason, want a combined list of all surnames and all facility names. Yes, this is a contrived example :-). Produce that list!

`members` table

https://i.imgur.com/BkIONKX.png

`facilities` table

https://i.imgur.com/cUIabdz.png

target output

https://i.imgur.com/QHPpyvL.png

???

* select surname from members union select name from facilities;
* select surname from members and select name from facilities;
* select members('surname') union select facilities('name');
* select surname from members as well as name from facilities;

