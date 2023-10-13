# FastAPI in Python Cheat Sheet 🚀🐍

Welcome to the FastAPI cheat sheet! FastAPI is a modern, fast, and highly productive web framework for building APIs with Python. Whether you're a beginner or an experienced developer, this cheat sheet will help you get started and explore its powerful features.

## Installation

You can install FastAPI and Uvicorn (ASGI server) using pip:

```python
pip install fastapi
pip install uvicorn
```

## Code Examples

### Hello, FastAPI!

Here's a simple FastAPI application that responds with "Hello, FastAPI!" for all requests:

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"message": "Hello, FastAPI!"}
```

### Path Parameters

FastAPI makes it easy to handle path parameters in your routes:

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/items/{item_id}")
def read_item(item_id: int, q: str = None):
    return {"item_id": item_id, "q": q}
```

### Request Bodies

You can parse request bodies with FastAPI:

```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

class Item(BaseModel):
    name: str
    description: str = None

@app.post("/items/")
def create_item(item: Item):
    return item
```

### Response Models

FastAPI allows you to define response models for your routes:

```python
from fastapi import FastAPI

app = FastAPI()

class Item:
    def __init__(self, name: str, description: str = None):
        self.name = name
        self.description = description

@app.get("/items/{item_id}", response_model=Item)
def read_item(item_id: int):
    return Item(name="Item Name", description="Item Description")
```

### Authentication and Authorization

Implement user authentication and authorization in your FastAPI application using OAuth2, JWT, and more.

### WebSocket Support

FastAPI supports WebSocket connections for real-time applications.

### File Uploads

You can handle file uploads in your FastAPI application.

### Dependency Injection

FastAPI provides dependency injection to manage complex dependencies in your routes.

### SQL Databases

Integrate SQL databases like SQLAlchemy with FastAPI for database-driven applications.

FastAPI is designed for ease of use and high performance, making it an excellent choice for building APIs. This cheat sheet provides an overview of FastAPI's capabilities and code examples to help you get started.

📖 FastAPI Documentation: [FastAPI Documentation](https://fastapi.tiangolo.com/)

Feel free to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and web development content. Enjoy your journey with FastAPI! 🚀🐍🌟
