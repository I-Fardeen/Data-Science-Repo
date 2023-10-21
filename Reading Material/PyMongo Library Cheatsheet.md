# PyMongo in Python Cheat Sheet 🐍🍃

Welcome to the PyMongo cheat sheet! PyMongo is the official Python driver for MongoDB. It allows you to interact with MongoDB databases seamlessly. Let's explore key concepts and code examples for PyMongo.

## Installation

You can install PyMongo using pip:

```bash
pip install pymongo
```

## Connecting to MongoDB

### Importing PyMongo

To start using PyMongo, import the library:

```python
import pymongo
```

### Creating a Connection

Connect to a MongoDB server:

```python
client = pymongo.MongoClient("mongodb://localhost:27017/")
```

## Working with Databases and Collections

### Creating a Database

Create or access a MongoDB database:

```python
db = client["mydatabase"]
```

### Creating a Collection

Create or access a collection within the database:

```python
collection = db["mycollection"]
```

## Inserting Documents

You can insert data into a collection:

```python
data = {"name": "John", "age": 30}
result = collection.insert_one(data)
```

## Querying Documents

Retrieve documents from a collection:

```python
query = {"name": "John"}
result = collection.find(query)

for document in result:
    print(document)
```

## Updating Documents

Update a document within a collection:

```python
query = {"name": "John"}
new_values = {"$set": {"age": 31}}
collection.update_one(query, new_values)
```

## Deleting Documents

Delete a document within a collection:

```python
query = {"name": "John"}
collection.delete_one(query)
```

## Resources

📖 Official Documentation: [PyMongo Documentation](https://pymongo.readthedocs.io/en/stable/)

Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data science-related content. Enjoy your journey with PyMongo! 🐍🍃🌟
