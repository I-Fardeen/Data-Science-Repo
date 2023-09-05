# MySQL Commands Cheat Sheet 🐬📜

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of MySQL! This cheat sheet provides essential MySQL commands and code examples to manage your databases. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more valuable content! 🙌

🌐 **Connect to a Database**:
Connect to a MySQL database using the `mysql` command-line tool.
```bash
mysql -u username -p
```

📚 **Show Databases**:
List all databases available on the MySQL server.
```sql
SHOW DATABASES;
```

➕ **Create a Database**:
Create a new database.
```sql
CREATE DATABASE mydb;
```

🏗️ **Use a Database**:
Select a database for use.
```sql
USE mydb;
```

🗃️ **Show Tables**:
List all tables in the selected database.
```sql
SHOW TABLES;
```

📋 **Describe a Table**:
View the structure of a table.
```sql
DESCRIBE tablename;
```

➡️ **Create a Table**:
Create a new table with specified columns and data types.
```sql
CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(255),
  email VARCHAR(255)
);
```

➕ **Insert Data**:
Add data into a table.
```sql
INSERT INTO users (username, email)
VALUES ('john_doe', 'john@example.com');
```

🔍 **Select Data**:
Retrieve data from a table.
```sql
SELECT * FROM users;
```

✏️ **Update Data**:
Modify existing data in a table.
```sql
UPDATE users
SET email = 'new_email@example.com'
WHERE username = 'john_doe';
```

❌ **Delete Data**:
Remove data from a table.
```sql
DELETE FROM users
WHERE username = 'john_doe';
```

🔑 **Add a New User**:
Create a new MySQL user.
```sql
CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';
```

🔒 **Grant Privileges**:
Assign privileges to a user for a specific database.
```sql
GRANT ALL PRIVILEGES ON mydb.* TO 'newuser'@'localhost';
```

🔓 **Revoke Privileges**:
Remove privileges from a user for a specific database.
```sql
REVOKE ALL PRIVILEGES ON mydb.* FROM 'newuser'@'localhost';
```

💾 **Backup a Database**:
Create a backup of a MySQL database.
```bash
mysqldump -u username -p mydb > backup.sql
```

🔄 **Restore a Database**:
Restore a MySQL database from a backup file.
```bash
mysql -u username -p mydb < backup.sql
```

Explore these MySQL commands and examples to efficiently manage your databases. Happy querying! 🚀🔍

Made with :heart: by **Fardeen Ahmad Khan**
