Chapter 3: Filtering Grouped Data

## Overview
In this chapter, we will explore filtering grouped data in SQL. We'll learn about the HAVING clause, which allows us to filter the results of aggregate functions and apply conditions to grouped data. We'll also dive into the order of execution and the difference between HAVING and WHERE clauses.

### Filtering Grouped Data
Combining filtering with grouping allows us to narrow down our results and extract meaningful insights from our data.

#### HAVING Clause
In SQL, we cannot use the WHERE clause to filter results based on aggregate functions. Instead, we use the HAVING clause, which is specifically designed for filtering grouped data. The HAVING clause is placed after the GROUP BY clause and allows us to apply conditions to the results of aggregate functions.

```sql
SELECT release_year
FROM films
GROUP BY release_year
HAVING COUNT(*) > 10;
```

#### Order of Execution
Understanding the order of execution is crucial when working with grouped data and filtering. The order of execution is as follows: FROM, WHERE, GROUP BY, HAVING, SELECT, ORDER BY, and LIMIT. This order determines which clauses are executed first and helps us write correct queries.

#### HAVING vs WHERE
The WHERE clause filters individual records, whereas the HAVING clause filters grouped records. When translating business questions into SQL queries, it's important to use the appropriate clause based on the nature of the question. WHERE is used for individual record filtering, while HAVING is used for filtering grouped data based on aggregate functions.

```sql
-- Using WHERE
SELECT title
FROM films
WHERE release_year = 2000;

-- Using HAVING
SELECT release_year, AVG(duration)
FROM films
GROUP BY release_year
HAVING AVG(duration) > 120;
```

