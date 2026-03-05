# Day 02 — Tables & Data Types

---

## What is a Table?

A table is where data is stored in a database.
It is made up of rows and columns — just like a spreadsheet.

- Columns define what type of data is stored (name, age, date etc)
- Rows are the actual data entries (one row = one record)

Example — a students table:

| id | name  | age | enrolled   |
|----|-------|-----|------------|
| 1  | Ali   | 22  | 2024-01-15 |
| 2  | Sara  | 20  | 2024-02-10 |
| 3  | Omar  | 23  | 2024-03-01 |

Each row is one student. Each column is one piece of information about that student.

---

## Creating a Table

To create a table you use CREATE TABLE and define each column with a name and a data type.

CREATE TABLE students (
    id       INT,
    name     VARCHAR(100),
    age      INT,
    enrolled DATE
);

---

## Data Types

When you create a column you must tell MySQL what kind of data it will hold.
This is called a data type. MySQL will only accept that type of data in that column.

INT
- Stores whole numbers (no decimals)
- Examples: 1, 25, 1000, -5
- Use for: id, age, quantity, year

VARCHAR(n)
- Stores text up to n characters long
- Examples: 'Ali', 'London', 'admin@email.com'
- Use for: names, emails, short text fields

TEXT
- Stores long text with no character limit
- Examples: blog posts, descriptions, comments
- Use for: anything that could be very long

DATE
- Stores a date in YYYY-MM-DD format
- Examples: 2024-01-15, 2023-12-31
- Use for: birthdays, enrollment dates, deadlines

BOOLEAN
- Stores TRUE or FALSE (MySQL stores this as 1 or 0)
- Examples: is_available, is_active, is_admin
- Use for: yes/no fields

DECIMAL(p, s)
- Stores numbers with decimals
- p = total digits, s = digits after the decimal point
- Example: DECIMAL(10, 2) stores up to 10 digits with 2 after the dot
- Use for: prices, salaries, measurements

---

## NULL vs Empty String

NULL means the value is completely missing — it was never given.
An empty string means the value was given but it is blank.

NULL   = no value at all
''     = a value was entered but it is empty

Example:
- A student with no phone number stored = NULL
- A student who typed nothing in the phone field = ''

These are different things. NULL is not zero, not false, not empty text.
It just means unknown or missing.

---
