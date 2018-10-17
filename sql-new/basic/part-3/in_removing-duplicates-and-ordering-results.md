---
author: amgando

aspects:
  - introduction

levels:
  - beginner

type: normal

category: must-know

standards:
  sql.read-single-table.0: 10
  sql.read-single-table.1: 10
  sql.read-single-table.2: 10
  sql.read-single-table.3: 10

links:

  - '[Removing duplicates, and ordering results](https://pgexercises.com/questions/basic/unique.html){documentation}'

---

# Removing duplicates, and ordering results

---
## Content

Specifying `DISTINCT` after `SELECT` removes duplicate rows from the result set. Note that this applies to rows: if row A has multiple columns, row B is only equal to it if the values in all columns are the same. As a general rule, don't use `DISTINCT` in a willy-nilly fashion - it's not free to remove duplicates from large query result sets, so do it as-needed.

Specifying `ORDER BY` (after the `FROM` and `WHERE` clauses, near the end of the query) allows results to be ordered by a column or set of columns (comma separated).

The `LIMIT` keyword allows you to limit the number of results retrieved. This is useful for getting results a page at a time, and can be combined with the `OFFSET` keyword to get following pages. This is the same approach used by MySQL and is very convenient - you may, unfortunately, find that this process is a little more complicated in other database systems.

---
## Practice

How can you produce an ordered list of the first 10 surnames in the members table? The list must not contain duplicates.

`members` table

![table](https://i.imgur.com/BkIONKX.png)

target output

![output](https://i.imgur.com/5mfDSgL.png)

???

* select distinct surname from members order by surname limit 10;
* select surname from members order by surname;
* select distinct surname from members order by surname;
* select distinct(surname) from members order(surname) limit(10);

---
## Revision

How can you produce an ordered list of the first 10 surnames in the members table? The list must not contain duplicates.

`members` table

![table](https://i.imgur.com/BkIONKX.png)

target output

![output](https://i.imgur.com/5mfDSgL.png)

???

* select distinct surname from members order by surname limit 10;
* select surname from members order by surname;
* select distinct surname from members order by surname;
* select distinct(surname) from members order(surname) limit(10);

