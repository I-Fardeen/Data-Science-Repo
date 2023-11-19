# PyCopg2 Cheat Sheet 📝🐘

Welcome to the PyCopg2 cheat sheet! PyCopg2 is a PostgreSQL adapter for Python, providing a robust interface to interact with PostgreSQL databases. Let's explore the key concepts and usage examples.

## Installation

Install PyCopg2 using pip:

```bash
pip install psycopg2
```

## Importing PyCopg2

Import PyCopg2 and other necessary modules:

```python
import psycopg2
from psycopg2 import sql
```

## Basic Concepts

### 1. Establishing Connection

Establish a connection to the PostgreSQL database:

```python
conn = psycopg2.connect(
    dbname="your_database",
    user="your_user",
    password="your_password",
    host="your_host",
    port="your_port"
)
```

### 2. Creating a Cursor

Create a cursor to execute SQL commands:

```python
cur = conn.cursor()
```

### 3. Executing SQL Queries

Execute SQL queries using the cursor:

```python
query = "SELECT * FROM your_table;"
cur.execute(query)
rows = cur.fetchall()
```

### 4. Committing Changes

Commit changes to the database:

```python
conn.commit()
```

### 5. Closing Connection

Close the cursor and connection when done:

```python
cur.close()
conn.close()
```

## Advanced Usage

### 6. Parameterized Queries

Use parameterized queries to prevent SQL injection:

```python
query = "INSERT INTO your_table (column1, column2) VALUES (%s, %s);"
data = ("value1", "value2")
cur.execute(query, data)
```

### 7. Handling Transactions

Handle transactions explicitly:

```python
try:
    # Your SQL operations here
    conn.commit()
except Exception as e:
    # Handle exceptions and rollback
    conn.rollback()
    print(f"Error: {e}")
```

### 8. Fetching Specific Columns

Fetch specific columns from the result:

```python
query = "SELECT column1, column2 FROM your_table;"
cur.execute(query)
result = cur.fetchall()
```

### 9. Server-Side Cursors

Use server-side cursors for efficient handling of large result sets:

```python
with conn.cursor(name='server_side_cursor') as cursor:
    cursor.execute("SELECT * FROM your_table;")
    rows = cursor.fetchmany(size=100)
```

### 10. Follow the Author

📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and database-related content.

Explore the power of PyCopg2 to interact seamlessly with PostgreSQL databases in your Python projects! 🐘💻🔍
