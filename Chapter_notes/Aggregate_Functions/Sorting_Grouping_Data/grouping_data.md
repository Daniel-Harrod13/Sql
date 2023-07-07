Chapter 2: Grouping Data

## Overview
In this chapter, we will explore grouping data in SQL. Grouping allows us to summarize data for specific groups and perform calculations on those groups using aggregate functions. We will learn about the GROUP BY clause, grouping by single and multiple fields, error handling, combining GROUP BY with ORDER BY, and the order of execution.

### Grouping Data
Grouping data allows us to summarize and analyze data for specific groups, providing valuable insights and statistics.

#### GROUP BY Single Fields
The GROUP BY clause is used to group data based on one or more fields. When grouping by a single field, we can use aggregate functions to calculate summary statistics for each group.

```sql
SELECT certification, AVG(duration)
FROM films
GROUP BY certification;
```

#### Error Handling
When using GROUP BY, it is important to include all non-aggregated fields in the GROUP BY clause. SQL will return an error if a field is selected without being grouped or aggregated.

```sql
SELECT certification, COUNT(*)
FROM films
GROUP BY certification;
```

#### GROUP BY Multiple Fields
GROUP BY can be used with multiple fields, similar to ORDER BY. The order in which the fields are specified affects the grouping of the data.

```sql
SELECT certification, language, COUNT(*)
FROM films
GROUP BY certification, language;
```

#### GROUP BY with ORDER BY
GROUP BY can be combined with ORDER BY to group the data, perform calculations, and then order the results based on specific criteria.

```sql
SELECT certification, COUNT(*) AS title_count
FROM films
GROUP BY certification
ORDER BY title_count DESC;
```

### Order of Execution
The GROUP BY clause is executed after the FROM clause and before all other clauses. The order of execution is as follows: FROM, GROUP BY, SELECT (including aggregate functions), ORDER BY, and LIMIT.

---

These are the chapter notes for Chapter 2: Grouping Data in SQL. Understanding how to group data and use aggregate functions allows for powerful data analysis and summary statistics.
