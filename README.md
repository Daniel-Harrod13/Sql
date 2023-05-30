# Sql
Sql notes and projects
Certainly! Here's a summary of the main points in a README-style format:

## SQL Style Guide

### Overview
This README provides an overview of SQL style best practices to improve the readability and maintainability of your code.

### 1. SQL formatting
- SQL is flexible with formatting, but poorly formatted code can be difficult to read.
- Sample code:
  ```
  SELECT title, release_year, country FROM films LIMIT 3;
  ```
- Best practice is to format SQL queries properly for improved readability.

### 2. Best practices
- Follow established SQL style guides to ensure consistent formatting.
- Sample code:
  ```
  SELECT title,
         release_year,
         country
  FROM films
  LIMIT 3;
  ```

### 3. Style guides
- SQL style guides provide standards for indentation, capitalization, and naming conventions.
- Different formatting styles exist, but following a guide, such as Holywell's, helps maintain consistency.

### 4. Semicolon
- Including a semicolon at the end of a query is considered best practice.
- It is unnecessary in PostgreSQL, but helpful for compatibility and indicating query termination.

### 5. Dealing with non-standard field names
- Occasionally, tables may have non-standard field names with spaces or special characters.
- Enclose such field names in double-quotes to indicate they refer to a single field.
- Sample code:
  ```
  SELECT "release year"
  FROM films
  LIMIT 3;
  ```

### 6. Why do we format?
- Adhering to SQL style guides improves collaboration and readability.
- It facilitates understanding and debugging of queries.
## Filtering Numbers

This section covers filtering data using SQL's `WHERE` clause with comparison operators to focus on specific numeric values.

### WHERE Clause

The `WHERE` clause allows us to filter data based on specific conditions, similar to selecting a coat from a closet based on its color. We can narrow down the data to only what is relevant to our business questions.

### Comparison Operators

To filter numeric values, we use comparison operators in conjunction with the `WHERE` clause. Here are some commonly used comparison operators:

- Greater than (`>`) operator: Selects values that are greater than a specified number.
- Less than (`<`) operator: Selects values that are less than a specified number.
- Less than or equal to (`<=`) operator: Selects values that are less than or equal to a specified number.
- Equal to (`=`) operator: Selects values that are equal to a specified number.
- Greater than or equal to (`>=`) operator: Selects values that are greater than or equal to a specified number.
- Not equal to (`<>` or `!=`) operator: Selects values that are not equal to a specified number.

### Filtering Examples

Here are some examples of filtering numeric values using the `WHERE` clause with comparison operators:

- Select films released after the year 1960:
```sql
SELECT *
FROM films
WHERE release_year > 1960;
```

- Select films released before the year 1960:
```sql
SELECT *
FROM films
WHERE release_year < 1960;
```

- Select films released during or before the year 1960:
```sql
SELECT *
FROM films
WHERE release_year <= 1960;
```

- Select films released in the year 1960:
```sql
SELECT *
FROM films
WHERE release_year = 1960;
```

- Select films excluding those released in the year 1960:
```sql
SELECT *
FROM films
WHERE release_year <> 1960;
```

### Filtering Strings

The `WHERE` clause with the equals (`=`) operator can also be used to filter string values. When filtering strings, enclose the string value in single quotation marks.

Example:
```sql
SELECT *
FROM films
WHERE country = 'Japan';
```

### Order of Execution

When using the `WHERE` clause along with other clauses like `LIMIT`, the order of execution is important. In the written query, the order is `SELECT`, `FROM`, `WHERE`, `LIMIT`. However, the actual execution order is `FROM`, `WHERE`, `SELECT`, `LIMIT`. Think of it as going to the closet, finding where the green coats are (filtering), and then selecting a limited number of them.


