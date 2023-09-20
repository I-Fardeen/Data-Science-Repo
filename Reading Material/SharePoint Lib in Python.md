# SharePoint Library in Python Cheat Sheet 🚀📂

Welcome to the world of SharePoint automation in Python! This cheat sheet will guide you through essential operations for interacting with SharePoint using Python. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and programming insights! 🙌

## Table of Contents 🗒️

1. [Introduction to SharePoint](#introduction-to-sharepoint)
2. [Connecting to SharePoint](#connecting-to-sharepoint)
3. [Working with Documents](#working-with-documents)
4. [Uploading Files](#uploading-files)
5. [Downloading Files](#downloading-files)
6. [List and Library Operations](#list-and-library-operations)
7. [Authentication](#authentication)
8. [Error Handling](#error-handling)
9. [Resources](#resources)

## 1. Introduction to SharePoint 📑

SharePoint is a web-based platform that provides document management and collaboration features. With Python, you can automate tasks and interact with SharePoint data.

## 2. Connecting to SharePoint 🔗

Connect to your SharePoint site:

```python
from shareplum import Site

site = Site('https://your-sharepoint-site.com', auth=('username', 'password'))
```

## 3. Working with Documents 📄

List and manipulate documents:

```python
# List all documents in a library
documents = site.List('Shared Documents')

# Access document properties
doc = documents.get_file('document.txt')
print(doc['Name'], doc['Modified'])
```

## 4. Uploading Files 📤

Upload files to SharePoint:

```python
# Upload a file to a library
with open('file.txt', 'rb') as file:
    documents.upload_file(file, folder='FolderName')
```

## 5. Downloading Files 📥

Download files from SharePoint:

```python
# Download a file
with open('downloaded_file.txt', 'wb') as file:
    doc.download(file)
```

## 6. List and Library Operations 🗂️

Perform operations on lists and libraries:

```python
# Create a new library
site.add_list('New Library')

# Create a new list
site.add_list('New List', description='Description of the list')
```

## 7. Authentication 🔐

Implement authentication methods:

```python
from requests.auth import HTTPBasicAuth

# Use HTTP Basic Authentication
site = Site('https://your-sharepoint-site.com', auth=HTTPBasicAuth('username', 'password'))
```

## 8. Error Handling 🐞

Handle exceptions that may occur during SharePoint operations:

```python
try:
    # SharePoint code here
except Exception as e:
    print(f"An error occurred: {e}")
```

## 9. Resources 📚

Explore the SharePlum library documentation and SharePoint API for more details:

- [SharePlum Documentation](https://github.com/kongzivk/shareplum)
- [SharePoint API Documentation](https://docs.microsoft.com/en-us/sharepoint/dev/)

Start automating SharePoint tasks with Python!

Happy SharePoint scripting! 🚀📂
```

This cheat sheet provides an introduction to SharePoint automation in Python and includes code examples for performing various SharePoint operations. It serves as a handy reference for working with SharePoint using Python.
