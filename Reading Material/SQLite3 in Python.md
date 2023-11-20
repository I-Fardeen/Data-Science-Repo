# SQLite3 in Python Cheat Sheet 📝🐍

Welcome to the SQLite3 in Python cheat sheet! SQLite is a lightweight, file-based database engine that can be seamlessly integrated into Python applications. Here's your guide to key concepts and usage examples.

## Installation

SQLite3 comes pre-installed with Python, so there's no need for additional installation.

## Importing SQLite3

Import the SQLite3 module:

```python
import sqlite3
```

## Basic Concepts

### 1. Connecting to a Database

Connect to an SQLite database:

```python
conn = sqlite3.connect('your_database.db')
```

### 2. Creating a Cursor

Create a cursor to execute SQL commands:

```python
cur = conn.cursor()
```

### 3. Creating a Table

Create a table in the database:

```python
cur.execute('''CREATE TABLE IF NOT EXISTS your_table
               (id INTEGER PRIMARY KEY, name TEXT, age INTEGER)''')
```

### 4. Inserting Data

Insert data into the table:

```python
data = (1, 'John Doe', 25)
cur.execute("INSERT INTO your_table VALUES (?, ?, ?)", data)
```

### 5. Querying Data

Query data from the table:

```python
cur.execute("SELECT * FROM your_table")
rows = cur.fetchall()
```

### 6. Updating Data

Update data in the table:

```python
new_age = 26
cur.execute("UPDATE your_table SET age = ? WHERE name = 'John Doe'", (new_age,))
```

### 7. Deleting Data

Delete data from the table:

```python
cur.execute("DELETE FROM your_table WHERE id = 1")
```

### 8. Committing Changes

Commit changes to the database:

```python
conn.commit()
```

### 9. Closing Connection

Close the cursor and connection when done:

```python
cur.close()
conn.close()
```

## Advanced Usage

### 10. Using Context Manager

Use a context manager to automatically commit and close:

```python
with sqlite3.connect('your_database.db') as conn:
    with conn.cursor() as cur:
        cur.execute("SELECT * FROM your_table")
        rows = cur.fetchall()
```

### 11. Handling Transactions

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

### 12. Follow the Author

📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and database-related content.

Explore the simplicity and efficiency of SQLite3 in Python for your data storage needs! 🐍💻🗄️
