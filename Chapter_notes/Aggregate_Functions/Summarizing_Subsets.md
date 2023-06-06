# Summarizing Subsets with Aggregate Functions

## Overview
In this section, we will learn how to combine our filtering skills with aggregate functions to gain further insights from our data. By using the WHERE clause along with aggregate functions, we can summarize subsets of our data based on specific conditions. This allows us to extract meaningful information and answer more specific questions about our dataset.

## Using WHERE with Aggregate Functions
The WHERE clause is executed before the SELECT statement in SQL, which means we can apply filtering conditions to our data before performing the aggregation. This allows us to calculate summaries based on specific subsets of our data. Here are some examples:

1. Average budget of movies made in 2010 or later:
```sql
SELECT AVG(budget)
FROM films
WHERE release_year >= 2010;
```

2. Total budget of movies made in 2010:
```sql
SELECT SUM(budget)
FROM films
WHERE release_year = 2010;
```

3. Smallest budget among movies made in 2010:
```sql
SELECT MIN(budget)
FROM films
WHERE release_year = 2010;
```

4. Highest budget among movies made in 2010:
```sql
SELECT MAX(budget)
FROM films
WHERE release_year = 2010;
```

5. Count of the number of budgets for movies made in 2010:
```sql
SELECT COUNT(budget)
FROM films
WHERE release_year = 2010;
```

## Rounding Values with the ROUND() Function
When working with numerical values, it's often useful to round the results to a specified decimal place for better readability or precision. In SQL, we can achieve this using the ROUND() function. The ROUND() function takes two parameters: the number to round and the decimal place to round to.

1. Rounding the average budget to two decimal places:
```sql
SELECT ROUND(AVG(budget), 2)
FROM films;
```

2. Rounding the average budget to a whole number (zero decimal places):
```sql
SELECT ROUND(AVG(budget), 0)
FROM films;
```
(Note: The second parameter is optional, and if omitted, the default value of 0 is used.)

3. Rounding to the left of the decimal point using a negative parameter:
```sql
SELECT ROUND(AVG(budget), -5)
FROM films;
```
(Note: A negative value for the decimal place parameter causes rounding to occur to the left of the decimal point.)

Please note that the ROUND() function can only be used with numerical fields.

To find the number of decades covered by the films table using `MIN()` and `MAX()` functions and alias it as `number_of_decades`, you can follow this SQL query:

```sql
SELECT 
  (MAX(release_year) - MIN(release_year)) / 10 AS number_of_decades
FROM films;
```

In this query, `MAX(release_year)` retrieves the maximum release year from the films table, `MIN(release_year)` retrieves the minimum release year, and `(MAX(release_year) - MIN(release_year)) / 10` calculates the difference between the maximum and minimum release years in terms of decades. The result is then aliased as `number_of_decades`.

Executing this query will give you the number of decades covered by the films table.

```sql
SELECT title, ROUND(duration / 60.0, 2) AS duration_hours
FROM films;
```

In this query, the `ROUND` function is used to round the `duration / 60.0` expression to two decimal places. The result will be the `duration_hours` column, which contains the rounded duration values.

Make sure to replace `films` with the actual name of your table and adjust other column names as necessary.
