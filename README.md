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

