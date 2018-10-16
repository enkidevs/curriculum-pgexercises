---
author: amgando

aspects:
  - introduction

category: must-know

standards:
  sql.read-single-table.0: 10
  sql.read-single-table.1: 10

links:

  - '[Working with dates](https://pgexercises.com/questions/basic/date.html){documentation}'

---

# Working with dates

---
## Content

SQL timestamps are formatted in descending order of magnitude: `YYYY-MM-DD HH:MM:SS.nnnnnn`. We can compare them just like we might a unix timestamp, although getting the differences between dates is a little more involved.

---
## Practice

How can you produce a list of members who joined after the start of September 2012? Return the memid, surname, firstname, and joindate of the members in question.

`members` table

![table](https://i.imgur.com/BkIONKX.png)

target output

![output](https://i.imgur.com/uh8p30g.png)

???

* select memid, surname, firstname, joindate from members where joindate >= '2012-09-01';
* select everything from members where joindate is recent;
* select memid, surname, firstname, joindate from members where joindate is greater than '20122-09-01';
* select memid, surname, firstname, joindate from members where greater(joindate, '20122-09-01');

---
## Revision


How can you produce a list of members who joined after the start of September 2012? Return the memid, surname, firstname, and joindate of the members in question.

`members` table

![table](https://i.imgur.com/BkIONKX.png)

target output

![output](https://i.imgur.com/uh8p30g.png)

???

* select memid, surname, firstname, joindate from members where joindate >= '2012-09-01';
* select everything from members where joindate is recent;
* select memid, surname, firstname, joindate from members where joindate is greater than '20122-09-01';
* select memid, surname, firstname, joindate from members where greater(joindate, '20122-09-01');
