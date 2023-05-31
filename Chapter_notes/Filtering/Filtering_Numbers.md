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

## Let's Practice!

Now it's time to practice filtering data using the `WHERE` clause with comparison operators. Use the provided examples as a guide to write your own queries and explore the data further.
