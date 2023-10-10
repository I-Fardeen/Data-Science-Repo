# Flask in Python Cheat Sheet 🌐🐍

Welcome to the Flask cheat sheet! Flask is a lightweight and versatile Python web framework that makes it easy to build web applications. Whether you're new to web development or a seasoned developer, this cheat sheet will help you get started with Flask and includes code examples to kickstart your web projects.

## Installation

You can install Flask using pip:

```python
pip install Flask
```

## Code Examples

### Hello, Flask!

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello_flask():
    return 'Hello, Flask!'

if __name__ == '__main__':
    app.run()
```

### Dynamic Routes

```python
from flask import Flask

app = Flask(__name__)

@app.route('/user/<name>')
def user_profile(name):
    return f'Hello, {name}!'

if __name__ == '__main__':
    app.run()
```

### Templates

```python
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html')

if __name__ == '__main__':
    app.run()
```

### Handling Forms

```python
from flask import Flask, render_template, request

app = Flask(__name__)

@app.route('/login', methods=['GET', 'POST'])
def login():
    if request.method == 'POST':
        username = request.form['username']
        password = request.form['password']
        # Handle form data

    return render_template('login.html')

if __name__ == '__main__':
    app.run()
```

### Database Integration

```python
from flask import Flask
from flask_sqlalchemy import SQLAlchemy

app = Flask(__name)
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///mydatabase.db'
db = SQLAlchemy(app)

class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    username = db.Column(db.String(80), unique=True, nullable=False)

if __name__ == '__main__':
    app.run()
```

This cheat sheet provides a taste of Flask's capabilities and code examples to get you started. Flask's simplicity and extensibility make it a great choice for web development, from small projects to complex applications.

📖 Flask Documentation: [Flask Documentation](https://flask.palletsprojects.com/)

Feel free to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and web development content. Enjoy your journey with Flask! 🚀🌐📝
