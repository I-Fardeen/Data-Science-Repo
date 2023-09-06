# MySQL with Python Cheat Sheet 🐍📜

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of MySQL database operations with Python! This cheat sheet provides essential MySQL commands and Python code examples to help you work with databases seamlessly. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more valuable content and updates! 🙌

🚀 **Getting Started**:
Before you start, make sure you have the MySQL Connector/Python library installed.
```python
import mysql.connector

# Establish a connection
connection = mysql.connector.connect(
    host="localhost",
    user="username",
    password="password",
    database="mydb"
)
```

🔍 **Executing Queries**:
You can execute SQL queries using a cursor.
```python
cursor = connection.cursor()

# Execute SQL query
cursor.execute("SELECT * FROM mytable")

# Fetch results
result = cursor.fetchall()

# Don't forget to commit changes
connection.commit()

# Close the cursor and connection
cursor.close()
connection.close()
```

➕ **Inserting Data**:
Add data to a table.
```python
cursor = connection.cursor()

# Insert data
sql = "INSERT INTO mytable (column1, column2) VALUES (%s, %s)"
values = ("value1", "value2")
cursor.execute(sql, values)

# Commit and close
connection.commit()
cursor.close()
```

✏️ **Updating Data**:
Modify existing data.
```python
cursor = connection.cursor()

# Update data
sql = "UPDATE mytable SET column1 = %s WHERE column2 = %s"
values = ("new_value", "criteria_value")
cursor.execute(sql, values)

# Commit and close
connection.commit()
cursor.close()
```

❌ **Deleting Data**:
Remove data from a table.
```python
cursor = connection.cursor()

# Delete data
sql = "DELETE FROM mytable WHERE column = %s"
value = "value_to_delete"
cursor.execute(sql, (value,))

# Commit and close
connection.commit()
cursor.close()
```

🌐 **Fetching Data**:
Retrieve data from a query.
```python
cursor = connection.cursor()

# Execute SQL query
cursor.execute("SELECT * FROM mytable")

# Fetch one row
row = cursor.fetchone()

# Fetch all rows
rows = cursor.fetchall()

# Close the cursor
cursor.close()
```

📋 **Using Prepared Statements**:
Prevent SQL injection by using prepared statements.
```python
cursor = connection.cursor(prepared=True)

# Execute prepared statement
stmt = "INSERT INTO mytable (column1, column2) VALUES (?, ?)"
data = ("value1", "value2")
cursor.execute(stmt, data)

# Commit and close
connection.commit()
cursor.close()
```

🔐 **Transaction Management**:
Manage transactions to ensure data consistency.
```python
connection.start_transaction()

try:
    # Your database operations here
    
    connection.commit()
except:
    connection.rollback()

# Close the connection
connection.close()
```

Explore these commands and examples to seamlessly work with MySQL databases in Python. Happy coding! 🐍📊

Made with :heart: by **Fardeen Ahmad Khan**

