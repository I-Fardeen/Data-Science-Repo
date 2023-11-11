# DataShader Cheat Sheet 🌐📊

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the DataShader cheat sheet! DataShader is a Python library for visualizing large datasets in real-time. It's a powerful tool for creating interactive, high-performance visualizations. Let's dive into DataShader with some code examples!

## Installation

You can install DataShader using pip:

```bash
pip install datashader
```

## Importing DataShader

Import DataShader like this:

```python
import datashader as ds
import datashader.transfer_functions as tf
```

## Basic Usage

### 1. Creating Canvas

Create a canvas to render your plots:

```python
cvs = ds.Canvas(plot_width=500, plot_height=500)
```

### 2. Aggregating Points

Aggregate points on the canvas:

```python
agg = cvs.points(df, 'x', 'y', ds.mean('value'))
```

### 3. Rendering Image

Render the aggregated image using the transfer function:

```python
img = tf.shade(agg, cmap=['lightblue', 'darkblue'], how='eq_hist')
```

### 4. Displaying Image

Display the rendered image:

```python
ds.utils.export_image(img, 'output', fmt='.png')
```

### 5. Interactive Plot

Create an interactive plot with Bokeh:

```python
from datashader.bokeh_ext import InteractiveImage

InteractiveImage(img)
```

### 6. Exporting to HTML

Export the interactive plot to HTML:

```python
ds.utils.export_image(img, 'output', fmt='.html')
```

## Advanced Usage

### 7. Customizing Color Maps

Create a custom color map for your plots:

```python
color_key = {'red': (0, 0, 0), 'green': (0, 255, 0), 'blue': (0, 0, 255)}
img = tf.shade(agg, cmap=color_key, how='eq_hist')
```

### 8. Adjusting Plot Size

Adjust the plot size for your canvas:

```python
cvs = ds.Canvas(plot_width=800, plot_height=800)
```

## Resources

- 📖 Official Documentation: [DataShader Documentation](https://datashader.readthedocs.io)
- 📦 PyPI Package: [DataShader on PyPI](https://pypi.org/project/datashader)
- 📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data science content.

DataShader is your go-to library for handling large datasets and creating stunning visualizations. Explore its capabilities and enhance your data visualization experience! 🌐📊🚀

Made with :heart: by **Fardeen Ahmad Khan**
