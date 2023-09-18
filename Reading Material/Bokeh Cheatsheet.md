# Data Visualization using Bokeh in Python Cheat Sheet 🚀📊

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of Data Visualization with Bokeh in Python! This cheat sheet will guide you through the basics of creating stunning visualizations using the Bokeh library. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and Data Science insights! 🙌

## Table of Contents 🗒️

1. [Introduction to Bokeh](#introduction-to-bokeh)
2. [Installation](#installation)
3. [Basic Plot](#basic-plot)
4. [Customizing Plots](#customizing-plots)
5. [Interactive Visualizations](#interactive-visualizations)
6. [Adding Widgets](#adding-widgets)
7. [Linking Plots](#linking-plots)
8. [Geographical Maps](#geographical-maps)
9. [Exporting Plots](#exporting-plots)
10. [Resources](#resources)

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
from bokeh.plotting import figure, show
from bokeh.tile_sources import get_provider

tile_provider = get_provider('CARTODBPOSITRON')
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
