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

  - '[More aggregation](https://pgexercises.com/questions/basic/agg2.html){documentation}'

---

# More aggregation

---
## Content

You can use a subquery to find out what the most recent `joindate` is. One possible subquery could return a scalar table - that is, a table with a single column and a single row. Since we have just a single value, we can substitute the subquery anywhere we might put a single constant value. In this case, we use it to complete the `WHERE` clause of a query to find a given member.

You might hope that you'd be able to do something like below:

```sql
select firstname, surname, max(joindate)
from cd.members
```

Unfortunately, this doesn't work. The `MAX` function doesn't restrict rows like the `WHERE` clause does - it simply takes in a bunch of values and returns the biggest one. The database is then left wondering how to pair up a long list of names with the single join date that's come out of the max function, and fails. Instead, you're left having to say 'find me the row(s) which have a join date that's the same as the maximum join date'.

There are other ways to get this job done - one example is below. In this approach, rather than explicitly finding out what the last joined date is, we simply order our members table in descending order of join date, and pick off the first one. Note that this approach does not cover the extremely unlikely eventuality of two people joining at the exact same time :-).

```sql
select firstname, surname, joindate
from cd.members
order by joindate desc
limit 1;
```

---
## Practice

You'd like to get the first and last name of the last member(s) who signed up - not just the date. How can you do that?

`members` table

![table](https://i.imgur.com/BkIONKX.png)

target output

![output](https://i.imgur.com/XaLWF7C.png)

???

* select firstname, surname, joindate from members where joindate = (select max(joindate) from members);
* select everything from members where joindate equals max(joindate) from members;
* select firstname, surname, joindate from members where joindate is equal to max(joindate) in members;
* select * from members where joindate = (select max(joindate) from members);

---
## Revision

You'd like to get the first and last name of the last member(s) who signed up - not just the date. How can you do that?

`members` table

![table](https://i.imgur.com/BkIONKX.png)

target output

![output](https://i.imgur.com/XaLWF7C.png)

???

* select firstname, surname, joindate from members where joindate = (select max(joindate) from members);
* select everything from members where joindate equals max(joindate) from members;
* select firstname, surname, joindate from members where joindate is equal to max(joindate) in members;
* select * from members where joindate = (select max(joindate) from members);