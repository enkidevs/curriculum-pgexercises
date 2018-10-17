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

links:

  - '[Simple aggregation](https://pgexercises.com/questions/basic/agg.html){documentation}'

---

# Simple aggregation

---
## Content

This is our first foray into SQL's aggregate functions. They're used to extract information about whole groups of rows, and allow us to easily ask questions like:

- What's the most expensive facility to maintain on a monthly basis?
- Who has recommended the most new members?
- How much time has each member spent at our facilities?

The `MAX` aggregate function is very simple: it receives all the possible values for joindate, and outputs the one that's biggest. There's a lot more power to aggregate functions.

---
## Practice

You'd like to get the signup date of your last member. How can you retrieve this information?

`members` table

![table](https://i.imgur.com/BkIONKX.png)

target output

![output](https://i.imgur.com/UZiKVSr.png)

???

* select max(joindate) as latest from members;
* select last joindate from members as latest;
* select last('joindate') from members;
* select latest joindate as max from members;

---
## Revision

You'd like to get the signup date of your last member. How can you retrieve this information?

`members` table

![table](https://i.imgur.com/BkIONKX.png)

target output

![output](https://i.imgur.com/UZiKVSr.png)

???

* select max(joindate) as latest from members;
* select last joindate from members as latest;
* select last('joindate') from members;
* select latest joindate as max from members;

