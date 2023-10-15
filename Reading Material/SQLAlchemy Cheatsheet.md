# SQLAlchemy in Python Cheat Sheet 🐍🗄️

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the SQLAlchemy cheat sheet! SQLAlchemy is a popular and powerful Object Relational Mapper (ORM) for Python. Whether you're new to SQLAlchemy or looking to refresh your knowledge, this cheat sheet will guide you through its core concepts and provide code examples to get you started.

## Installation

You can install SQLAlchemy using pip:

```python
pip install sqlalchemy
```

## Code Examples

### Connecting to a Database

Establish a connection to a database and create a session:

```python
from sqlalchemy import create_engine
from sqlalchemy.orm import sessionmaker

# Create an engine
engine = create_engine('sqlite:///mydatabase.db')

# Create a session
Session = sessionmaker(bind=engine)
session = Session()
```

### Defining a Table

Define a table using SQLAlchemy's declarative base:

```python
from sqlalchemy import Column, Integer, String
from sqlalchemy.ext.declarative import declarative_base

Base = declarative_base()

class User(Base):
    __tablename__ = 'users'
    id = Column(Integer, primary_key=True)
    name = Column(String)
    age = Column(Integer)
```

### Creating and Querying Data

Create, add, and query data from the database:

```python
# Create a new user
new_user = User(name="John", age=30)

# Add the user to the session
session.add(new_user)

# Commit the changes to the database
session.commit()

# Query the database
user = session.query(User).filter_by(name="John").first()
```

### Relationships

Define relationships between tables:

```python
from sqlalchemy import ForeignKey
from sqlalchemy.orm import relationship

class Address(Base):
    __tablename__ = 'addresses'
    id = Column(Integer, primary_key=True)
    email = Column(String, nullable=False)
    user_id = Column(Integer, ForeignKey('users.id'))

User.addresses = relationship("Address", order_by=Address.id, back_populates="user")

# Accessing user's addresses
user_addresses = user.addresses
```

### ORM Queries

Perform various queries with SQLAlchemy's ORM:

```python
# SELECT
user = session.query(User).filter_by(name="John").first()

# UPDATE
user.age = 31

# DELETE
session.delete(user)
```

### Migrations

Manage database schema changes and migrations with tools like Alembic.

SQLAlchemy provides a powerful and flexible way to work with databases in Python. This cheat sheet offers an overview of essential SQLAlchemy concepts and code examples to help you get started.

📖 SQLAlchemy Documentation: [SQLAlchemy Documentation](https://docs.sqlalchemy.org/)

Feel free to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and database-related content. Happy coding! 🐍🗄️🌟

Made with :heart: by **Fardeen Ahmad Khan**
