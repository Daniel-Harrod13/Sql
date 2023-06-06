## Arithmetic Operations

Arithmetic operations in SQL allow us to perform calculations on numerical values within our queries. The basic arithmetic operators are:

- Addition: `+`
- Subtraction: `-`
- Multiplication: `*`
- Division: `/`

These operators can be used to perform calculations on columns, constants, or expressions. For example:

```sql
SELECT column1 + column2 AS sum_result
FROM table;
```

In this example, the `+` operator is used to add the values of `column1` and `column2`, and the result is given the alias `sum_result`.

## Division and Precision

When performing division in SQL, the precision of the result depends on the data types involved. If both the dividend and divisor are integers, SQL assumes integer division and returns an integer result, truncating any decimal places. To obtain more precise results, you can use decimal numbers in the division operation. For example:

```sql
SELECT 10.0 / 3.0 AS precise_result;
```

In this case, the division operation involves decimal numbers, resulting in a more precise decimal value.

## Difference between Aggregate Functions and Arithmetic

Aggregate functions, such as `SUM`, `MIN`, `MAX`, and `AVG`, operate vertically on a column, performing calculations on multiple rows and returning a single result. They are useful for summarizing data across a dataset.

Arithmetic operations, on the other hand, perform calculations horizontally within a row or between different columns. They are used to manipulate and transform data within each row of the result set.

## Aliasing with AS

Aliasing allows us to assign temporary names to the columns or calculated values in the result set. This is particularly useful when the resulting column doesn't have a meaningful name by default or when we want to provide a more descriptive name.

The `AS` keyword is used to assign an alias. For example:

```sql
SELECT (gross - budget) AS profit
FROM films;
```

In this query, the subtraction operation `(gross - budget)` is given the alias `profit`. The alias is used to provide a clear and descriptive name for the calculated column.

## Order of Execution and Aliasing

In SQL, the order of execution is important when using aliases. The `FROM` and `WHERE` clauses are executed before the `SELECT` clause. This means that aliases created in the `SELECT` clause are not available in the `WHERE` clause.

If you need to filter or conditionally aggregate based on an alias, you can use a subquery or a derived table. These constructs allow you to first create the alias in the inner query and then refer to it in the outer query.

Overall, understanding the order of execution and properly using aliases can help in creating more readable and efficient SQL queries.



To find the number of decades covered by the films table using `MIN()` and `MAX()` functions and alias it as `number_of_decades`, you can follow this SQL query:

```sql
SELECT 
  (MAX(release_year) - MIN(release_year)) / 10 AS number_of_decades
FROM films;
```

In this query, `MAX(release_year)` retrieves the maximum release year from the films table, `MIN(release_year)` retrieves the minimum release year, and `(MAX(release_year) - MIN(release_year)) / 10` calculates the difference between the maximum and minimum release years in terms of decades. The result is then aliased as `number_of_decades`.

Executing this query will give you the number of decades covered by the films table.




Your query to round `duration_hours` to two decimal places looks correct. By dividing `duration` by 60.0 and aliasing it as `duration_hours`, you have transformed the duration from minutes to hours. To round it to two decimal places, you can use the `ROUND` function. Here's an updated version of your query:

```sql
SELECT title, ROUND(duration / 60.0, 2) AS duration_hours
FROM films;
```

In this query, the `ROUND` function is used to round the `duration / 60.0` expression to two decimal places. The result will be the `duration_hours` column, which contains the rounded duration values.

Make sure to replace `films` with the actual name of your table and adjust other column names as necessary.
