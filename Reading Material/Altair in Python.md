# Altair in Python Cheat Sheet 📊🐍

Welcome to the Altair cheat sheet! Altair is a Python library for declarative data visualization. It's built on top of Vega and Vega-Lite, providing an elegant and concise way to create interactive visualizations. Let's explore Altair with code examples.

## Installation

You can install Altair using pip:

```bash
pip install altair
```

## Importing Altair

To start using Altair, import it:

```python
import altair as alt
```

## Creating Visualizations

Altair makes it easy to create various types of visualizations. Here's a simple example of creating a scatter plot:

```python
import pandas as pd

data = pd.DataFrame({'x': [1, 2, 3, 4, 5], 'y': [5, 4, 3, 2, 1]})

chart = alt.Chart(data).mark_point().encode(
    x='x',
    y='y'
)

chart
```

## Customizing Visualizations

You can customize visualizations with various encoding options. Here's an example of a bar chart with a custom color:

```python
data = pd.DataFrame({'Category': ['A', 'B', 'C'], 'Value': [5, 10, 8]})

chart = alt.Chart(data).mark_bar().encode(
    x='Category',
    y='Value',
    color=alt.value('blue')
)

chart
```

## Interactivity

Altair supports interactive elements in your visualizations. Here's an example of adding a tooltip:

```python
data = pd.DataFrame({'x': ['A', 'B', 'C'], 'y': [5, 10, 8]})

chart = alt.Chart(data).mark_bar().encode(
    x='x',
    y='y',
    tooltip=['x', 'y']
)

chart
```

## Resources

📖 Official Documentation: [Altair Documentation](https://altair-viz.github.io/)

Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data science content. Altair is a fantastic library for creating beautiful and interactive visualizations in Python! 📊🐍🌟
