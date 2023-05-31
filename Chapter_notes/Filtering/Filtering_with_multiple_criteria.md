## Filtering with Multiple Criteria

In this section, we'll learn how to apply multiple criteria to our filters in SQL queries.

### Introduction

There are situations where we need to meet more than one condition to filter our data effectively. For example, if we want to narrow down our coat choices, we might look for coats that are yellow and shorter in length.

### OR, AND, and BETWEEN

To enhance our filters and work with multiple criteria, we'll learn about three keywords: `OR`, `AND`, and `BETWEEN`.

- `OR` allows us to filter based on multiple conditions and requires only one condition to be satisfied.
- `AND` requires all conditions to be satisfied for the filter to be applied.
- `BETWEEN` is used to filter values within a specified range.

### Using the OR Operator

When using the `OR` operator, we combine it with the `WHERE` clause to filter based on multiple criteria. For example, let's say we want to select films released in either 1994 or 2000:

```sql
SELECT *
FROM films
WHERE release_year = 1994 OR release_year = 2000;
```

Make sure to specify the field for every `OR` condition.

### Using the AND Operator

The `AND` operator is used when we want all conditions to be satisfied in our filter. For example, if we want to select films released between 1994 and 2000:

```sql
SELECT *
FROM films
WHERE release_year >= 1994 AND release_year <= 2000;
```

Specify the field name separately for each `AND` condition.

### Combining AND and OR Operators

We can combine `AND` and `OR` operators to create more complex filters. For example, if we want to filter films released in 1994 or 1995 and have a certification of either PG or R:

```sql
SELECT *
FROM films
WHERE (release_year = 1994 OR release_year = 1995)
  AND (certification = 'PG' OR certification = 'R');
```

Enclose the individual clauses in parentheses to ensure the correct execution order.

### Using the BETWEEN Operator

The `BETWEEN` keyword provides a shorthand for filtering values within a specified range. It is inclusive, meaning it includes the beginning and end values. For example, to get the titles of all films released between 1994 and 2000:

```sql
SELECT *
FROM films
WHERE release_year BETWEEN 1994 AND 2000;
```

### Combining BETWEEN, AND, and OR

The `BETWEEN` clause can also be used with multiple `AND` and `OR` operators to create more powerful queries. For example, to get the titles of all films released between 1994 and 2000 from the United Kingdom:

```sql
SELECT *
FROM films
WHERE release_year BETWEEN 1994 AND 2000
  AND country = 'United Kingdom';
```

Remember to enclose individual clauses in parentheses for correct execution order.

## Let's Practice!

Now it's time to practice applying multiple criteria in your SQL queries. Use the examples provided as a guide to filter and retrieve the desired data from the database.
