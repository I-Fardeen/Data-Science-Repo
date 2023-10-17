# Plotnine in Python Cheat Sheet 🐍📊

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Plotnine cheat sheet! Plotnine is a Python data visualization library based on the Grammar of Graphics. This cheat sheet will help you get started with creating beautiful and informative plots using Plotnine.

## Installation

You can install Plotnine using pip:

```bash
pip install plotnine
```

## Code Examples

### Basic Plot

To create a basic scatter plot with Plotnine:

```python
from plotnine import ggplot, aes, geom_point

(ggplot(df)          # Specify the dataframe
 + aes(x='x', y='y')  # Define aesthetics
 + geom_point()       # Specify the geometry (plot type)
)
```

### Customizing Plots

You can customize your plots with various themes, scales, and labels:

```python
from plotnine import theme, scale_x_continuous, scale_y_continuous, labs

(ggplot(df)
 + aes(x='x', y='y')
 + geom_point()
 + theme_minimal()  # Apply a minimal theme
 + scale_x_continuous(name='X-axis Label')  # Customize X-axis label
 + scale_y_continuous(name='Y-axis Label')  # Customize Y-axis label
 + labs(title='Customized Scatter Plot')  # Add a plot title
)
```

### Bar Plot

To create a bar plot with Plotnine:

```python
from plotnine import geom_bar

(ggplot(df)
 + aes(x='category', y='value')
 + geom_bar(stat='identity')
)
```

### Line Plot

To create a line plot with Plotnine:

```python
from plotnine import geom_line

(ggplot(df)
 + aes(x='x', y='y')
 + geom_line()
)
```

### Saving Plots

You can save your plots to various formats (e.g., PNG, PDF) using the `ggsave` function:

```python
from plotnine import ggsave

plot = (ggplot(df)
        + aes(x='x', y='y')
        + geom_point())

ggsave(plot, 'my_plot.png', dpi=300)
```

### Faceting

Faceting allows you to create multiple plots based on a categorical variable:

```python
from plotnine import facet_wrap

(ggplot(df)
 + aes(x='x', y='y')
 + geom_point()
 + facet_wrap('~category')
)
```

Plotnine is a versatile data visualization library that makes it easy to create various types of plots in Python. This cheat sheet provides code examples to help you get started.

📖 Plotnine Documentation: [Plotnine Documentation](https://plotnine.readthedocs.io/en/stable/)

Feel free to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data visualization-related content. Happy plotting! 🐍📊🌟

Made with :heart: by **Fardeen Ahmad Khan**
