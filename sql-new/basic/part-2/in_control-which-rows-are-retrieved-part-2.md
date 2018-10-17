---
author: amgando

aspects:
  - introduction

levels:
  - beginner

category: must-know

standards:
  sql.read-single-table.0: 10
  sql.read-single-table.1: 10
  sql.read-single-table.2: 10

links:

  - '[Control which rows are retrieved - part 2](https://pgexercises.com/questions/basic/where2.html){documentation}'

---

# Control which rows are retrieved - part 2

---
## Content

The `WHERE` clause allows us to filter for the rows we're interested in.

When we want to test for two or more conditions, we use `AND` to combine them. We can, as you might expect, use `OR` to test whether either of a pair of conditions is true.

You might have noticed that this is our first query that combines a `WHERE` clause with selecting specific columns. This may not seem too interesting now, but as we add in more complex operations like joins later, you'll see the simple elegance of this behaviour.

---
## Practice

How can you produce a list of facilities that charge a fee to members, and that fee is less than 1/50th of the monthly maintenance cost? Return the facid, facility name, member cost, and monthly maintenance of the facilities in question.

`facilities` table

![table](https://i.imgur.com/cUIabdz.png)

target output

![output](https://i.imgur.com/yfPSxft.png)

visualisation

![visualisation](https://i.imgur.com/ZyETk6n.png)

???

* select facid, name, membercost, monthlymaintenance from facilities where membercost > 0 and membercost < monthlymaintenance/50.0;
* select four columns from facilities where membercost greater than 0 and membercost less than monthlymaintenance divided by 50;
* select facid, name, membercost, monthlymaintenance from facilities where greater(membercost, 0) and less(membercost, monthlymaintenance/50.0);
* select * from facilities where membercost > 0 and membercost < monthlymaintenance/50.0;

---
## Revision

How can you produce a list of facilities that charge a fee to members, and that fee is less than 1/50th of the monthly maintenance cost? Return the facid, facility name, member cost, and monthly maintenance of the facilities in question.

`facilities` table

![table](https://i.imgur.com/cUIabdz.png)

target output

![output](https://i.imgur.com/yfPSxft.png)

visualisation

![visualisation](https://i.imgur.com/ZyETk6n.png)

???

* select facid, name, membercost, monthlymaintenance from facilities where membercost > 0 and membercost < monthlymaintenance/50.0;
* select four columns from facilities where membercost greater than 0 and membercost less than monthlymaintenance divided by 50;
* select facid, name, membercost, monthlymaintenance from facilities where greater(membercost, 0) and less(membercost, monthlymaintenance/50.0);
* select * from facilities where membercost > 0 and membercost < monthlymaintenance/50.0;

