# Day 03 — INSERT & SELECT

---

## What is INSERT?

INSERT is the command you use to add data into a table.
Without INSERT, your table is just empty columns with no records.

Every time you want to add a new row to a table, you use INSERT.

---

## INSERT Syntax

INSERT INTO table_name (column1, column2, column3)
VALUES (value1, value2, value3);

Example — adding one student:

INSERT INTO students (id, name, age, enrolled)
VALUES (1, 'Ali', 22, '2024-01-15');

Rules:
- The columns and values must match in order
- Text and dates go inside single quotes
- Numbers do not need quotes
- You must follow the data type you set for each column

---

## Inserting Multiple Rows

You can insert more than one row at a time by separating each set of values with a comma.

INSERT INTO students (id, name, age, enrolled)
VALUES
(1, 'Ali',  22, '2024-01-15'),
(2, 'Sara', 20, '2024-02-10'),
(3, 'Omar', 23, '2024-03-01');

---

## What is SELECT?

SELECT is the command you use to read data from a table.
It is the most used command in SQL — almost everything involves a SELECT.

SELECT does not change any data. It just retrieves and displays it.

---

## SELECT Syntax

-- Get every column from a table
SELECT * FROM students;

-- Get only specific columns
SELECT name, age FROM students;

The * means all columns.
If you only want certain columns, list them by name separated by commas.

---

## SELECT is Non-Destructive

SELECT never changes, deletes, or modifies your data.
It is completely safe to run as many times as you want.
Think of it as just looking at the data, not touching it.

---

## My Notes

Write your own thoughts here after reading.
What confused you? What clicked? What do you want to remember?
