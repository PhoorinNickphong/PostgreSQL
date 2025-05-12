# 240-216 Computer Engineering Laboratory
# 🛢️ PostgreSQL Practice

This repository is intended for learning and experimenting with **PostgreSQL**, an advanced open-source relational database system. The purpose is to practice SQL queries, understand PostgreSQL features, and prepare for integrating databases in full-stack applications.

---

## 🧠 What’s Inside

This repo may include or be expanded to include:

- SQL scripts for table creation, data insertion, and complex queries
- Example ER diagrams and schema design
- Sample connection code using Python (psycopg2)
- Basic to advanced SQL commands
- Notes and documentation on PostgreSQL syntax

---

## 🔧 Requirements

To get started with PostgreSQL locally:

- Install PostgreSQL: [https://www.postgresql.org/download/](https://www.postgresql.org/download/)
- Optionally use a GUI client:
  - pgAdmin
  - DBeaver
  - TablePlus

---

## ▶️ Sample Usage

Connect to PostgreSQL using `psql` CLI:

```bash
psql -U postgres -d mydatabase
```

Run a SQL script:

```bash
\i init_schema.sql
```

---

## 🔗 Python Example

```python
import psycopg2

conn = psycopg2.connect(
    dbname="mydatabase",
    user="postgres",
    password="yourpassword",
    host="localhost",
    port="5432"
)

cur = conn.cursor()
cur.execute("SELECT * FROM students;")
rows = cur.fetchall()
for row in rows:
    print(row)

cur.close()
conn.close()
```

---

## 📌 Goals

- Learn core SQL with PostgreSQL
- Practice writing efficient queries
- Prepare for backend integration


