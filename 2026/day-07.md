# Day 07 — Aggregate Functions

---

## What are Aggregate Functions?

Aggregate functions are special functions that take a group of rows
and calculate a single result from them.

Instead of returning one row per record, they return one value
that summarises all the rows.

Example — instead of listing every student's age,
COUNT() tells you how many students there are in total.

---

## COUNT()

COUNT counts how many rows exist in a result.

-- count all rows in the table
SELECT COUNT(*) FROM students;

-- count only rows where age is not NULL
SELECT COUNT(age) FROM students;

COUNT(*) counts every row including NULLs.
COUNT(column) only counts rows where that column has a value.

---

## SUM()

SUM adds up all the values in a column.
Only works on number columns.

-- total of all ages
SELECT SUM(age) FROM students;

-- total value of all orders
SELECT SUM(amount) FROM orders;

---

## AVG()

AVG calculates the average of all values in a column.
Only works on number columns.

-- average age of all students
SELECT AVG(age) FROM students;

-- average order amount
SELECT AVG(amount) FROM orders;

---

## MAX()

MAX returns the highest value in a column.

-- oldest student
SELECT MAX(age) FROM students;

-- most expensive product
SELECT MAX(price) FROM products;

-- latest enrollment date
SELECT MAX(enrolled) FROM students;

---

## MIN()

MIN returns the lowest value in a column.

-- youngest student
SELECT MIN(age) FROM students;

-- cheapest product
SELECT MIN(price) FROM products;

-- earliest enrollment date
SELECT MIN(enrolled) FROM students;

---

## Using Multiple Aggregate Functions Together

You can use multiple aggregate functions in the same query.

-- get a full summary of the students table
SELECT
    COUNT(*) AS total_students,
    AVG(age)  AS average_age,
    MAX(age)  AS oldest,
    MIN(age)  AS youngest
FROM students;

---

## AS — Giving a Result a Name

When you use aggregate functions the column name in the result
is just the function itself which looks messy.
You can use AS to give it a cleaner name.

Without AS:
COUNT(*)
22

With AS:
total_students
22

Example:
SELECT COUNT(*) AS total_students FROM students;

---

## My Notes

Write your own thoughts here after reading.
What confused you? What clicked? What do you want to remember?
