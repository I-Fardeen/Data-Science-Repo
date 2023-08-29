# Matplotlib.pyplot Cheat Sheet 📊

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Matplotlib.pyplot Cheat Sheet! 🌟 Matplotlib is a powerful library for creating visualizations in Python. This cheat sheet provides a quick reference for creating various types of plots using `matplotlib.pyplot`.

## Importing Matplotlib
```python
import matplotlib.pyplot as plt
```

## Basic Line Plot 📈
Create a basic line plot with x and y values.

```python
plt.plot(x_values, y_values, label='Label')
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')
plt.title('Title')
plt.legend()
plt.show()
```

## Scatter Plot 🌸
Create a scatter plot with x and y values.

```python
plt.scatter(x_values, y_values, label='Label', color='color', marker='marker')
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')
plt.title('Title')
plt.legend()
plt.show()
```

## Bar Plot 📊
Create a bar plot with x and y values.

```python
plt.bar(x_values, y_values, label='Label', color='color')
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')
plt.title('Title')
plt.legend()
plt.show()
```

## Histogram 📊
Create a histogram to visualize the distribution of data.

```python
plt.hist(data, bins=number_of_bins, color='color', edgecolor='edgecolor')
plt.xlabel('X-axis Label')
plt.ylabel('Frequency')
plt.title('Title')
plt.show()
```

## Pie Chart 🍰
Create a pie chart to show the distribution of categorical data.

```python
plt.pie(data, labels=labels, autopct='%1.1f%%', startangle=90)
plt.title('Title')
plt.axis('equal')
plt.show()
```

## Customize Plot Appearance 🎨
Customize plot appearance using various options.

- 🎨 **Color**:
```python
color='color'
```

- 🎨 **Marker Styles**:
```python
marker='marker_style'
```

- 🎨 **Line Styles**:
```python
linestyle='line_style'
```

- 🎨 **Legend**:
```python
plt.legend(loc='location')
```

Matplotlib offers extensive options to customize your plots. This cheat sheet covers only a fraction of what `matplotlib.pyplot` offers. Explore the Matplotlib documentation for more functions and customization options.

Feel free to refer to this cheat sheet whenever you're creating visualizations with Matplotlib. Happy plotting! 🚀

Made with :heart: by **Fardeen Ahmad Khan**
