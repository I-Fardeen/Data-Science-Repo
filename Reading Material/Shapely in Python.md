# Shapely in Python Cheat Sheet 🌐🐍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Shapely cheat sheet! Shapely is a Python library used for geometric object manipulation and analysis. It's a great tool for working with various geometric shapes and performing spatial operations. This guide will introduce you to the basics of Shapely with code examples.

## Installation

You can install Shapely using pip:

```bash
pip install shapely
```

## Importing Shapely

To start using Shapely, import it:

```python
from shapely.geometry import Point, Polygon, LineString
```

## Creating Geometric Objects

You can create various geometric objects using Shapely:

### Point

```python
point = Point(0, 0)
```

### LineString

```python
line = LineString([(0, 0), (1, 1), (2, 0)])
```

### Polygon

```python
polygon = Polygon([(0, 0), (0, 1), (1, 1), (1, 0)])
```

## Geometric Operations

Shapely offers a wide range of geometric operations, such as:

### Area

```python
polygon.area
```

### Length

```python
line.length
```

### Intersection

```python
result = line.intersection(polygon)
```

### Union

```python
result = polygon.union(line)
```

## Validity Checks

You can check the validity of geometric objects:

```python
polygon.is_valid
```

## Geometric Predicates

Shapely allows you to check relationships between geometric objects:

```python
polygon.contains(point)
```

## Buffering

You can create a buffer around geometric objects:

```python
buffered_polygon = polygon.buffer(0.2)
```

## Resources

📖 Official Documentation: [Shapely Documentation](https://shapely.readthedocs.io/en/stable/manual.html)

Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data science content. Shapely is a powerful library for working with geometric objects in Python! 🌐🐍🌟

Made with :heart: by **Fardeen Ahmad Khan**
