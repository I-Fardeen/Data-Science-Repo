# OS Library in Python Cheat Sheet 🚀🐍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of OS manipulation in Python using the OS library! This cheat sheet will guide you through essential operations for working with files and directories. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and programming insights! 🙌

## Table of Contents 🗒️

1. [Introduction to the OS Library](#introduction-to-the-os-library)
2. [Checking and Manipulating Directories](#checking-and-manipulating-directories)
3. [Working with Files](#working-with-files)
4. [File and Directory Information](#file-and-directory-information)
5. [Path Manipulation](#path-manipulation)
6. [Directory Traversal](#directory-traversal)
7. [Running System Commands](#running-system-commands)
8. [File Permissions](#file-permissions)
9. [Error Handling](#error-handling)
10. [Resources](#resources)

## 1. Introduction to the OS Library 🚀

The OS library in Python allows you to interact with the operating system, perform file and directory operations, and run system commands.

## 2. Checking and Manipulating Directories 📂

Create, remove, and navigate directories:

```python
import os

# Create a directory
os.mkdir('my_directory')

# Remove a directory
os.rmdir('my_directory')

# Change current working directory
os.chdir('/path/to/new/directory')
```

## 3. Working with Files 📄

Create, rename, copy, and delete files:

```python
# Create a file
with open('my_file.txt', 'w') as file:
    file.write('Hello, World!')

# Rename a file
os.rename('old_file.txt', 'new_file.txt')

# Copy a file
os.copy('source.txt', 'destination.txt')

# Delete a file
os.remove('file_to_delete.txt')
```

## 4. File and Directory Information 📊

Retrieve information about files and directories:

```python
# Get file size
file_size = os.path.getsize('my_file.txt')

# Check if a path is a file or directory
is_file = os.path.isfile('my_file.txt')
is_dir = os.path.isdir('my_directory')
```

## 5. Path Manipulation 🛤️

Manipulate file paths:

```python
# Join paths
full_path = os.path.join('/path', 'to', 'file.txt')

# Split path
directory, filename = os.path.split('/path/to/file.txt')
```

## 6. Directory Traversal 🚶‍♂️

Traverse directories and list files:

```python
# List files in a directory
file_list = os.listdir('/path/to/directory')

# Recursively traverse directories
for root, dirs, files in os.walk('/path/to/start/directory'):
    for file in files:
        print(os.path.join(root, file))
```

## 7. Running System Commands 🖥️

Run system commands from Python:

```python
import subprocess

# Run a system command
output = subprocess.check_output(['ls', '-l'])
```

## 8. File Permissions 🔐

Check and modify file permissions:

```python
# Check if a file is readable
is_readable = os.access('my_file.txt', os.R_OK)

# Change file permissions
os.chmod('my_file.txt', 0o777)
```

## 9. Error Handling 🐞

Handle exceptions that may occur during OS operations:

```python
try:
    os.mkdir('my_directory')
except OSError as e:
    print(f"An error occurred: {e}")
```

## 10. Resources 📚

Explore the Python documentation and tutorials for more details:

- [Python OS Module Documentation](https://docs.python.org/3/library/os.html)

Start working with files and directories using the OS library in Python!

Happy coding! 🚀🐍

Made with :heart: by **Fardeen Ahmad Khan**
