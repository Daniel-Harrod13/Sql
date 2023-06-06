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
