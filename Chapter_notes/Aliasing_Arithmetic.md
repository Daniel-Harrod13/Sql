# Aliasing and Arithmetic in SQL

## Overview
In this lesson, we will explore how to use arithmetic operations in SQL queries and learn about aliasing using the `AS` keyword. Arithmetic operations allow us to perform calculations on numerical values within our queries, while aliasing helps us assign temporary names to the results of these calculations or columns in the result set.

## Arithmetic Operations
SQL supports basic arithmetic operations such as addition (+), subtraction (-), multiplication (*), and division (/). Here are some examples:

```sql
SELECT (5 + 3) AS sum;
SELECT (10 - 5) AS difference;
SELECT (4 * 6) AS product;
SELECT (10 / 3) AS division_result;
```

Note that the use of parentheses is optional in simple arithmetic expressions, but they can be used to explicitly indicate the order of operations.

## Division and Precision
When performing division in SQL, be aware of the data types involved. If you divide an integer by another integer, SQL assumes that you want to get an integer result. For example, `10 / 3` would give a result of `3` rather than `3.33`.

To get more precise results, you can introduce decimal places by using numbers with decimal points in your division operation. For example:

```sql
SELECT (4.0 / 3.0) AS precise_result;
```

This will give you the expected decimal result of `1.33`.

## Difference between Aggregate Functions and Arithmetic
Aggregate functions, such as `SUM`, operate vertically on a column, performing calculations on multiple rows and returning a single result. On the other hand, arithmetic operations perform calculations horizontally, combining values from different columns or performing calculations within a single row.

The key difference is that aggregate functions summarize data across multiple records, while arithmetic operations perform calculations on a row-by-row basis.

## Aliasing with AS
When performing calculations or using aggregate functions, the resulting column in the query output may not have a meaningful name. In such cases, it is recommended to use aliases to assign a clear and descriptive name to the column.

Aliases can be created using the `AS` keyword, followed by the desired name. For example:

```sql
SELECT (gross - budget) AS profit
FROM films;
```

Here, the alias `profit` is assigned to the result of the subtraction operation between the `gross` and `budget` columns.

## Order of Execution and Aliasing
When using aliases in SQL queries, it's important to understand the order of execution. Aliases are created in the `SELECT` clause, which is executed after the `FROM` and `WHERE` clauses.

Therefore, you cannot refer to an alias in the `WHERE` clause or any earlier part of the query. If you need to filter or conditionally aggregate based on an alias, you can use a subquery or a derived table.

## Conclusion
In this lesson, we learned about using arithmetic operations in SQL queries and the importance of aliasing to provide meaningful names to the calculated columns or results. We explored arithmetic operations like addition, subtraction, multiplication, and division, along with the need to consider precision when performing division. Additionally, we discussed the difference between aggregate functions and arithmetic and the order of execution when using aliases in SQL queries.
