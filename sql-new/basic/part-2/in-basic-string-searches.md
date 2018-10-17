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

  - '[Basic string searches](https://pgexercises.com/questions/basic/where3.html){documentation}'

---

# Basic string searches

---
## Content

SQL's `LIKE` operator provides simple pattern matching on strings. It's pretty much universally implemented, and is nice and simple to use - it just takes a string with the `%` character matching any string, and `_` matching any single character.

There are other ways to accomplish this task: Postgres supports regular expressions with the `~` operator, for example. Use whatever makes you feel comfortable, but do be aware that the `LIKE` operator is much more portable between systems.

---
## Practice

How can you produce a list of all facilities with the word 'Tennis' in their name?

`facilities` table

![table](https://i.imgur.com/cUIabdz.png)

target output

![output](https://i.imgur.com/Ie2tLwh.png)

???

* select * from facilities where name like '%Tennis%';
* select everything from facilities where name like 'Tennis';
* select * from facilities where name like('%Tennis%')
* select * from facilities where name % Tennis

---
## Revision

How can you produce a list of all facilities with the word 'Tennis' in their name?

`facilities` table

![table](https://i.imgur.com/cUIabdz.png)

target output

![output](https://i.imgur.com/Ie2tLwh.png)

???

* select * from facilities where name like '%Tennis%';
* select everything from facilities where name like 'Tennis';
* select * from facilities where name like('%Tennis%')
* select * from facilities where name % Tennis
