---
dg-publish: true
dg-permalink: "202302100011"
aliases:
  - Structured query language
  - SQL
tags:
  - computer-science/data
  - computer-science/data/data-engineering
  - computer-science
file-created: 2023-02-10
file-modified: 2023-10-10
note-type: 
description: 
linter-yaml-title-alias: Structured query language
source: 
---

# Structured query language

#status/done

---

See also [[Programming and SQL Practice|Programming and sql practice]]

> [!ai]+ AI
>
> SQL stands for Structured Query Language, and it is a programming language used for managing and manipulating relational databases. It is designed to retrieve, insert, update, and delete data from databases. SQL commands are used to interact with the database, such as creating tables, inserting data, and querying information. It provides a standardized way to communicate with databases across different platforms and is widely used in web development, data analysis, and other applications that involve working with large datasets.

It's the language used to query data in and is a necessary skills when working with data warehouses. It works by defining what we wish to retrieve, which tables it should come from, filtering them and ordering them.

## Optimizing SQL queries

There are various ways of making efficient queries. Long story short - simpler joins tend to be most efficient while using advanced techniques such as correlated subqueries are cost more resources.

We can use the EXPLAIN command to determine how the database engine is interpreting the information.
- [Optimize query computation  |  BigQuery  |  Google Cloud](https://cloud.google.com/bigquery/docs/best-practices-performance-compute)

The performance of different types of joins are are compared here:
- [8 Different Ways to Join Tables in SQL and its Time Complexity | by Mengyong Lee | Towards Data Science](https://towardsdatascience.com/sql-complexity-and-8-different-ways-to-join-tables-22ed7ae0060c#:~:text=TLDR%3A%20The%20most%20efficient%20join,methods%20of%20joins%2C%20read%20further.&text=Relational%20algebra%20is%20the%20most,natural%20way%20to%20do%20so.)
- [Day 3: The Twelve Days of SQL: There isn’t always a single optimal query plan for a SQL query | So Many Oracle Manuals, So Little Time](https://iggyfernandez.wordpress.com/2011/12/02/day-3-twelve-days-of-sql-there-isnt-always-a-single-optimal-query-plan-for-a-sql-query/)

## SQL Subqueries

1. **Scalar Subquery**: Returns a single value and is often used in the SELECT clause or comparisons.

   ```sql
   SELECT column1, (SELECT MAX(column2) FROM table2) AS max_value
   FROM table1;
   ```

2. **Row Subquery**: Returns a single row of data and is typically used in the FROM clause for joining.

   ```sql
   SELECT column1
   FROM table1
   WHERE (column1, column2) = (SELECT column1, column2 FROM table2);
   ```

3. **Table Subquery**: Returns a result set and acts as a virtual table in the main query.

   ```sql
   SELECT column1
   FROM table1
   WHERE column2 IN (SELECT column2 FROM table2 WHERE column3 = 'value');
   ```

4. **Correlated Subquery**: References outer query columns and is executed for each row of the outer query.

   ```sql
   SELECT column1
   FROM table1 AS t1
   WHERE column2 > (SELECT AVG(column2) FROM table1 AS t2 WHERE t1.column3 = t2.column3);
   ```

5. **Nested Subquery**: Embedded subquery within another subquery, used for complex queries.

   ```sql
   SELECT column1
   FROM table1
   WHERE column2 IN (SELECT column2 FROM table2 WHERE column3 = (SELECT MAX(column4) FROM table3));
   ```
