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

  - '[SELECT queries 101](https://sqlbolt.com/lesson/select_queries_introduction){documentation}'

---

# Queries with constraints

---
## Content

In order to filter certain results from being returned, we need to use a WHERE clause in the query. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.

```sql
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;
```

---
## Practice

SQL let's you filter queries using the `WHERE` clause so you can focus on only the data you need.

???

* True
* False

---
## Revision

SQL let's you combine multiple conditions in a `WHERE` clause in case you want to use multiple rules to filter data before retrieval.

???

* True
* False

