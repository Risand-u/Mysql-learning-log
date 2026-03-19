# Day 06 — Sorting & Limiting

---

## What is ORDER BY?

ORDER BY is the clause you use to sort your results.
By default MySQL does not guarantee any particular order when you SELECT data.
If you want results in a specific order you must use ORDER BY.

---

## ORDER BY Syntax

SELECT * FROM table_name
ORDER BY column_name ASC;

SELECT * FROM table_name
ORDER BY column_name DESC;

ASC  = ascending order  (smallest to biggest, A to Z, oldest to newest)
DESC = descending order (biggest to smallest, Z to A, newest to oldest)

If you do not write ASC or DESC, MySQL defaults to ASC.

---

## ORDER BY Examples

-- sort students from youngest to oldest
SELECT * FROM students
ORDER BY age ASC;

-- sort students from oldest to youngest
SELECT * FROM students
ORDER BY age DESC;

-- sort students alphabetically by name A to Z
SELECT * FROM students
ORDER BY name ASC;

-- sort students alphabetically by name Z to A
SELECT * FROM students
ORDER BY name DESC;

---

## Sorting by Multiple Columns

You can sort by more than one column.
MySQL sorts by the first column first, then uses the second column to break ties.

-- sort by age first, then by name if ages are the same
SELECT * FROM students
ORDER BY age ASC, name ASC;

---

## What is LIMIT?

LIMIT restricts how many rows are returned in your result.
Without LIMIT you get every matching row.
With LIMIT you only get the number of rows you ask for.

---

## LIMIT Syntax

SELECT * FROM table_name
LIMIT number;

Example — get only the first 5 students:

SELECT * FROM students
LIMIT 5;

---

## Combining ORDER BY and LIMIT

ORDER BY and LIMIT are very powerful together.
This combination is how you do things like top 3, newest 5, lowest 10.

-- get the 3 oldest students
SELECT * FROM students
ORDER BY age DESC
LIMIT 3;

-- get the 5 most recently enrolled students
SELECT * FROM students
ORDER BY enrolled DESC
LIMIT 5;

-- get the 1 youngest student
SELECT * FROM students
ORDER BY age ASC
LIMIT 1;

---

## Order of Clauses

In a SELECT statement the clauses must come in this order:

SELECT
FROM
WHERE
ORDER BY
LIMIT

Example:

SELECT * FROM students
WHERE age > 18
ORDER BY age DESC
LIMIT 5;

---

## My Notes

Write your own thoughts here after reading.
What confused you? What clicked? What do you want to remember?
