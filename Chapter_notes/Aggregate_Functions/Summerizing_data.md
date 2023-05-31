# Summarizing Data with Aggregate Functions

## Description
This README provides an overview of SQL aggregate functions used to summarize data. It covers the concepts of aggregate functions, including COUNT(), AVERAGE(), SUM(), MIN(), and MAX(), and explains how to use them to derive meaningful insights from your dataset.

## Table of Contents
- [Aggregate Functions](#aggregate-functions)
- [Numerical and Non-Numerical Data](#numerical-and-non-numerical-data)
- [Alias for Summarized Data](#alias-for-summarized-data)

## Aggregate Functions
When analyzing data, it's often useful to summarize the dataset as a whole rather than examining individual records. SQL provides aggregate functions that perform calculations on multiple values and return a single result. We'll cover four new aggregate functions in addition to the familiar COUNT():

- AVERAGE(): Calculates the average value of a specified field.
- SUM(): Computes the sum of the values in a field.
- MIN(): Finds the minimum value in a field.
- MAX(): Identifies the maximum value in a field.

## Numerical and Non-Numerical Data
While some aggregate functions require numerical fields (AVERAGE() and SUM()), others can be used with both numerical and non-numerical fields. For non-numerical fields, COUNT(), MIN(), and MAX() operate by considering the records themselves rather than performing arithmetic calculations.

```sql
-- Example: Average budget of films
SELECT AVG(budget)
FROM films;

-- Example: Total budget of all films
SELECT SUM(budget)
FROM films;

-- Example: Lowest budget among films
SELECT MIN(budget)
FROM films;

-- Example: Highest budget among films
SELECT MAX(budget)
FROM films;
```

## Alias for Summarized Data
When using aggregate functions, the resulting field name in the output is automatically updated to match the function name (e.g., "min" for MIN()). It's considered good practice to use an alias to provide a more descriptive name for the summarized data. Aliasing makes the results clear and understandable for anyone reading the code.

```sql
-- Example: Alias for average budget
SELECT AVG(budget) AS average_budget
FROM films;
```

