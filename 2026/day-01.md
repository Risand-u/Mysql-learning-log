# Day 01 — What is a Database?

---

## What is a Database?

A database is organised storage for data.
Instead of saving everything in random files, a database keeps data in structured tables.
Each table holds one type of thing — like students, products, or orders.

Example — a school database might have:
- A students table
- A courses table
- A grades table

Each table stores its own data but they can all be linked together.

---

## What is a DBMS?

DBMS stands for Database Management System.
It is the software that runs and manages the database.
MySQL is a DBMS. So is PostgreSQL, SQLite, and Oracle.

Without a DBMS, your data is just sitting there doing nothing.
The DBMS is what lets you create tables, insert data, search, update, and delete.

---

## What is SQL?

SQL stands for Structured Query Language.
It is the language you use to talk to a relational database.
It is not like Python or JavaScript — it does not build apps.
It only does one job: communicate with a database.

Examples:

SHOW DATABASES;         -- show all databases
CREATE DATABASE school; -- create a new database
USE school;             -- switch to using it

---

## Relational vs Non-Relational

Relational Database:
- Stores data in tables with rows and columns
- Tables can be linked together using keys
- Uses SQL to query data
- Examples: MySQL, PostgreSQL, SQLite

Non-Relational Database (NoSQL):
- Stores data in other formats like documents or key-value pairs
- More flexible, no fixed table structure
- Examples: MongoDB, Redis, Firebase

MySQL is relational. Everything we learn — tables, joins, keys — is based on this model.

---

## Why MySQL?

- Free and open source
- Used in the real world by companies like Facebook, Twitter, YouTube
- SQL skills learned here transfer to PostgreSQL, SQLite, and others
- Comes with MySQL Workbench — a visual tool to write and run queries



