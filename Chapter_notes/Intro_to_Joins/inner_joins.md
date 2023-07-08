# Chapter 4: INNER JOIN

## Overview
In this chapter, we will explore the INNER JOIN operation in SQL. INNER JOIN is one of the most commonly used joins and allows us to combine data from multiple tables based on a matching condition. We will learn the syntax of INNER JOIN, understand how it works, and apply it to real-world examples.

### The Ins and Outs of INNER JOIN
We'll start by understanding the basics of INNER JOIN and how it combines data from two tables based on a shared key field. We'll visualize the matching records and learn about the key field's significance. The concept of INNER JOIN will be demonstrated using a simple example.

**Example:**
```sql
SELECT *
FROM left_table
INNER JOIN right_table
  ON left_table.id = right_table.id;
```

### The Leadership Database Schema
We'll work with a database schema that contains tables related to world leaders. The schema includes tables such as presidents, prime_ministers, monarchs, states, and prime_minister_terms. We'll explore this database schema throughout the chapter.

### Querying Tables
We'll begin by querying the presidents table to retrieve all fields using the asterisk (*) symbol. This will give us an overview of the data in the presidents table. Additionally, we'll examine a snippet of the prime_ministers table.

**Example:**
```sql
SELECT *
FROM presidents;
```

### Joining Tables with INNER JOIN
We'll explore the need to join tables, specifically when we are interested in countries that have both a president and a prime minister. We'll use the INNER JOIN operation to combine the presidents and prime_ministers tables based on the "country" field. The step-by-step syntax of INNER JOIN will be explained, and we'll select the desired fields to be returned. The result of the INNER JOIN will be displayed, showing the countries that have both presidents and prime ministers.

**Example:**
```sql
SELECT p1.country, p1.name AS president_name, p2.name AS prime_minister_name
FROM presidents AS p1
INNER JOIN prime_ministers AS p2
  ON p1.country = p2.country;
```

### Aliasing Tables and Using the USING Command
To make our query more concise, we'll learn about aliasing table names using the AS keyword. This allows us to use shorter aliases for the table names in our query. Additionally, we'll introduce the USING command, which is a shortcut to join tables based on identical column names. This simplifies the join condition and reduces the amount of repetitive code in our query.

**Example:**
```sql
SELECT p1.country, p1.name AS president_name, p2.name AS prime_minister_name
FROM presidents AS p1
INNER JOIN prime_ministers AS p2
  USING (country);
```

---

These are the chapter notes for Chapter 4: INNER JOIN in SQL. Understanding how to join tables using INNER JOIN is crucial for combining data from multiple sources. This chapter provides a solid foundation for working with INNER JOIN and lays the groundwork for more advanced join operations in SQL.
