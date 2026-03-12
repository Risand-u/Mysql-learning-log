# Day 04 — UPDATE & DELETE

---

## What is UPDATE?

UPDATE is the command you use to change existing data in a table.
You use it when a record already exists but something about it needs to change.

Example — a student changed their age, or an email address was entered wrong.
Instead of deleting and re-adding the row, you just UPDATE it.

---

## UPDATE Syntax

UPDATE table_name
SET column1 = value1, column2 = value2
WHERE condition;

Example — update one student's age:

UPDATE students
SET age = 23
WHERE id = 1;

Example — update multiple columns at once:

UPDATE students
SET age = 23, enrolled = '2024-06-01'
WHERE id = 1;

---

## The WHERE Clause in UPDATE

The WHERE clause tells MySQL which row or rows to update.
If you leave out WHERE, MySQL will update every single row in the table.

This is one of the most dangerous mistakes in SQL.

WITHOUT WHERE — updates every row:
UPDATE students SET age = 99;

WITH WHERE — updates only the matching row:
UPDATE students SET age = 99 WHERE id = 1;

Always double check your WHERE clause before running an UPDATE.

---

## What is DELETE?

DELETE is the command you use to remove rows from a table.
It permanently removes the data — there is no undo.

---

## DELETE Syntax

DELETE FROM table_name
WHERE condition;

Example — delete one student:

DELETE FROM students
WHERE id = 1;

---

## The WHERE Clause in DELETE

Same rule as UPDATE — if you forget WHERE, you delete everything.

WITHOUT WHERE — deletes every row in the table:
DELETE FROM students;

WITH WHERE — deletes only the matching row:
DELETE FROM students WHERE id = 1;

The table itself still exists after DELETE.
Only the rows are removed, not the table structure.

---

## UPDATE vs DELETE

UPDATE — changes data inside a row, the row stays
DELETE — removes the entire row from the table

---

## My Notes

Write your own thoughts here after reading.
What confused you? What clicked? What do you want to remember?
