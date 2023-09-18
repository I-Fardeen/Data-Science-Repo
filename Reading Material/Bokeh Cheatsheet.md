# Data Visualization using Bokeh in Python Cheat Sheet 🚀📊

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of Data Visualization with Bokeh in Python! This cheat sheet will guide you through the basics of creating stunning visualizations using the Bokeh library. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and Data Science insights! 🙌

## Table of Contents 🗒️

1. [Introduction to Bokeh](#1-introduction-to-bokeh-)
2. [Installation](#2-installation-)
3. [Basic Plot](#3-basic-plot-)
4. [Customizing Plots](#4-customizing-plots-)
5. [Interactive Visualizations](#5-interactive-visualizations-)
6. [Adding Widgets](#6-adding-widgets-)
7. [Linking Plots](#7-linking-plots-)
8. [Geographical Maps](#8-geographical-maps-)
9. [Exporting Plots](#9-exporting-plots-)
10. [Resources](#10-resources-)

## 1. Introduction to Bokeh 🚀

Bokeh is a powerful Python library for interactive data visualization. It's ideal for creating web-ready, interactive, and visually appealing plots and dashboards.

## 2. Installation 📦

Install Bokeh using pip:

```bash
pip install bokeh
```

## 3. Basic Plot 📈

Create a simple Bokeh plot:

```python
from bokeh.plotting import figure, show

# Create a figure
p = figure()

# Add data
p.circle([1, 2, 3, 4, 5], [6, 7, 2, 4, 5])

# Show the plot
show(p)
```

## 4. Customizing Plots 🎨

Customize your plots with titles, labels, and colors:

```python
p = figure(title="My Custom Plot", x_axis_label="X-axis", y_axis_label="Y-axis")
p.line([1, 2, 3, 4, 5], [6, 7, 2, 4, 5], line_color="red", line_width=2)
```

## 5. Interactive Visualizations 🔄

Create interactive plots with tooltips, hover effects, and more:

```python
from bokeh.models import HoverTool

hover = HoverTool(tooltips=[("X", "$x"), ("Y", "$y")])
p.add_tools(hover)
```

## 6. Adding Widgets 🧩

Enhance your plots with widgets like sliders and buttons:

```python
from bokeh.models import Slider

slider = Slider(start=0, end=10, value=5, step=1, title="Slider")
```

## 7. Linking Plots 🔗

Link multiple plots for synchronized interactions:

```python
from bokeh.layouts import gridplot

grid = gridplot([[p1, p2], [p3, p4]])
```

## 8. Geographical Maps 🗺️

Create interactive geographical maps with Bokeh's GeoJSON support:

```python
# Import necessary modules
from bokeh.plotting import figure, show
from bokeh.tile_sources import get_provider
from bokeh.models import GeoJSONDataSource

# Create a figure with a tile source (CARTO Positron)
tile_provider = get_provider('CARTODBPOSITRON')
p = figure(title="Geographical Map", plot_height=400, plot_width=600,
           x_range=(-2000000, 6000000), y_range=(-1000000, 7000000),
           tools='pan, wheel_zoom, reset', toolbar_location="above")
p.add_tile(tile_provider)

# Define GeoJSON data (replace 'your_geojson_file.geojson' with your data)
geojson_data = GeoJSONDataSource(geojson=open('your_geojson_file.geojson').read())

# Add GeoJSON patches to the plot (customize color, line color, etc.)
p.patches('xs', 'ys', source=geojson_data, fill_color='blue', line_color='white', line_width=0.5, alpha=0.7)

# Show the plot
show(p)
```

## 9. Exporting Plots 📷

Export your Bokeh plots as standalone HTML files:

```python
from bokeh.io import output_file

output_file("my_plot.html")
show(p)
```

## 10. Resources 📚

Explore the Bokeh documentation and tutorials for advanced techniques and examples:

- [Bokeh Documentation](https://docs.bokeh.org/en/latest/index.html)
- [Bokeh Gallery](https://docs.bokeh.org/en/latest/docs/gallery.html)

Start creating beautiful and interactive visualizations with Bokeh in Python today!

Happy plotting! 📊🚀

Made with :heart: by **Fardeen Ahmad Khan**
