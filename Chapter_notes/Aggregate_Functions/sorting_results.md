## Overview
In this chapter, we will learn about sorting results in SQL to gain further insight into our data. Sorting allows us to put our data in a specific order, making it easier to understand and analyze. We will explore the ORDER BY keyword, sorting in ascending and descending order, sorting by multiple fields, and the order of execution.

### Sorting Results
Sorting results helps us quickly see our data in a specific sequence, making it easier to analyze and interpret.

#### ORDER BY
The ORDER BY keyword is used to sort results based on one or more fields. By default, the sorting is done in ascending order, from smallest to largest or from A to Z.

```sql
SELECT budget
FROM films
ORDER BY budget;
```

#### ASCending
To explicitly specify ascending order, we can include the ASC keyword in our query.

```sql
SELECT budget
FROM films
ORDER BY budget ASC;
```

#### DESCending
To sort results in descending order, we use the DESC keyword.

```sql
SELECT title
FROM films
WHERE budget IS NOT NULL
ORDER BY budget DESC;
```

### Sorting Fields
We can sort results based on fields without including them in the SELECT statement. However, it is recommended to include the field being sorted for clarity.

```sql
SELECT title
FROM films
ORDER BY release_year;
```

### ORDER BY Multiple Fields
ORDER BY can be used to sort results based on multiple fields, allowing for more precise sorting. The fields are separated by commas, and the sorting is done based on the order specified.

```sql
SELECT title, imdb_score
FROM films
ORDER BY oscar_wins, imdb_score DESC;
```

### Different Orders
We can select different orders for each field being sorted, providing flexibility in sorting criteria.

```sql
SELECT name, birthdate
FROM actors
ORDER BY birthdate ASC, name DESC;
```

### Order of Execution
The ORDER BY clause is executed after the SELECT statement and before the LIMIT clause. The order of execution is as follows: FROM, WHERE, SELECT, ORDER BY, LIMIT.

---
