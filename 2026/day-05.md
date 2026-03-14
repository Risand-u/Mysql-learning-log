# Day 05 — Filtering with WHERE

---

## What is WHERE?

WHERE is the clause you use to filter data.
It tells MySQL which rows you want to work with.
You use it with SELECT, UPDATE, and DELETE.

Without WHERE you get every row.
With WHERE you only get the rows that match your condition.

---

## Basic WHERE Syntax

SELECT * FROM table_name
WHERE condition;

Example — get only students who are 22 years old:

SELECT * FROM students
WHERE age = 22;
 
---

## Comparison Operators

These are the symbols you use to build your conditions.

=       equal to
!=      not equal to
>       greater than
<       less than
>=      greater than or equal to
<=      less than or equal to

Examples:

SELECT * FROM students WHERE age = 22;
SELECT * FROM students WHERE age != 22;
SELECT * FROM students WHERE age > 20;
SELECT * FROM students WHERE age < 25;
SELECT * FROM students WHERE age >= 18;
SELECT * FROM students WHERE age <= 30;

---

## BETWEEN

BETWEEN filters rows where a value is within a range.
It is inclusive — meaning it includes the start and end values.

SELECT * FROM students
WHERE age BETWEEN 18 AND 25;

This returns students aged 18, 19, 20, 21, 22, 23, 24, and 25.

---

## LIKE

LIKE is used to search for a pattern inside text.
You use it with two special characters:

%   matches any number of characters (including zero)
_   matches exactly one character

Examples:

-- names that start with A
SELECT * FROM students WHERE name LIKE 'A%';

-- names that end with i
SELECT * FROM students WHERE name LIKE '%i';

-- names that contain the letter a anywhere
SELECT * FROM students WHERE name LIKE '%a%';

-- names that are exactly 3 characters long
SELECT * FROM students WHERE name LIKE '___';

---

## IN

IN lets you filter by a list of values instead of writing multiple conditions.

Without IN:
SELECT * FROM students WHERE age = 18 OR age = 20 OR age = 22;

With IN — much cleaner:
SELECT * FROM students WHERE age IN (18, 20, 22);

Works with text too:

SELECT * FROM students WHERE name IN ('Ali', 'Sara', 'Omar');

---

## Combining Conditions with AND and OR

AND — both conditions must be true
OR  — at least one condition must be true

Examples:

SELECT * FROM students WHERE age > 18 AND age < 25;
SELECT * FROM students WHERE name = 'Ali' OR name = 'Sara';

---

