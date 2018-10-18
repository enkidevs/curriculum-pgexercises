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

links:

  - '[Classify results into buckets](https://pgexercises.com/questions/basic/classify.html){documentation}'

---

# Classify results into buckets

---
## Content

We can do some computation in the area of the query between `SELECT` and `FROM`. You can put anything in here that will produce a single result per returned row - including subqueries.

We can also use something called a `CASE` statement. `CASE` is effectively like if/switch statements in other languages. To add a 'middle' option, we would simply insert another `when ... then` section below:

```sql
select name,
	case when (monthlymaintenance > 100) then
		'expensive'
	else
		'cheap'
	end as cost
	from facilities;
```

There's also the `AS` operator. This is used to label columns or expressions to make them display more nicely or to make them easier to reference when used as part of a subquery.

---
## Practice

How can you produce a list of facilities, with each labelled as 'cheap' or 'expensive' depending on if their monthly maintenance cost is more than $100? Return the name and monthly maintenance of the facilities in question.

`facilities` table

https://i.imgur.com/cUIabdz.png

target output

https://i.imgur.com/m9KL1IG.png

???

* select name, case when (monthlymaintenance > 100) then 'expensive' else 'cheap' end as cost from facilities;
* select everything from facilities where 'expensive' or 'cheap';
* select name, expensive, cheap from facilities;
* select name, case when true then 'expensive' else 'cheap' from facilities;

---
## Revision

How can you produce a list of facilities, with each labelled as 'cheap' or 'expensive' depending on if their monthly maintenance cost is more than $100? Return the name and monthly maintenance of the facilities in question.

`facilities` table

https://i.imgur.com/cUIabdz.png

target output

https://i.imgur.com/m9KL1IG.png

???

* select name, case when (monthlymaintenance > 100) then 'expensive' else 'cheap' end as cost from facilities;
* select everything from facilities where 'expensive' or 'cheap';
* select name, expensive, cheap from facilities;
* select name, case when true then 'expensive' else 'cheap' from facilities;

