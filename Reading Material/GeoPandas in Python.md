# GeoPandas Cheat Sheet 🗺️🐍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the GeoPandas cheat sheet! GeoPandas is an open-source Python library that simplifies working with geospatial data. Whether you're a GIS professional or a data scientist, GeoPandas has you covered. Let's explore GeoPandas with some code examples!

## Installation

You can install GeoPandas along with its dependencies using pip:

```bash
pip install geopandas
```

## Importing GeoPandas

To start using GeoPandas, import it as follows:

```python
import geopandas as gpd
```

## Basic Operations

### 1. Reading Spatial Data

You can read spatial data from various formats such as Shapefiles, GeoJSON, and more:

```python
gdf = gpd.read_file('your_shapefile.shp')
```

### 2. Viewing Data

Use the `.head()` method to display the first few rows of your GeoDataFrame:

```python
print(gdf.head())
```

### 3. Plotting

GeoPandas provides easy plotting capabilities:

```python
gdf.plot()
```

## Spatial Operations

### 4. Spatial Filtering

Filter data using spatial conditions:

```python
filtered_data = gdf[gdf['column_name'] == 'some_value']
```

### 5. Buffering

Create buffer zones around your spatial data:

```python
buffered = gdf.buffer(distance=0.01)
```

### 6. Spatial Joins

Perform spatial joins between GeoDataFrames:

```python
result = gpd.sjoin(gdf1, gdf2, how='inner', op='intersects')
```

## Geometric Operations

### 7. Area and Length Calculations

Compute area and length of geometries:

```python
gdf['area'] = gdf.geometry.area
gdf['length'] = gdf.geometry.length
```

### 8. Centroids

Calculate centroids of geometries:

```python
gdf['centroid'] = gdf.geometry.centroid
```

## Visualization

### 9. Custom Plotting

Customize your plots with Matplotlib:

```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots(1, 1, figsize=(10, 10))
gdf.plot(column='column_to_visualize', cmap='coolwarm', ax=ax)
```

### 10. Interactive Maps

GeoPandas is compatible with interactive mapping libraries like Folium and Bokeh.

## Resources

- 📖 Official Documentation: [GeoPandas Documentation](https://geopandas.org/en/stable/index.html)
- 📦 PyPI Package: [GeoPandas on PyPI](https://pypi.org/project/geopandas/)
- 📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data science content.

GeoPandas empowers you to work with geospatial data effortlessly. Explore the world through data! 🌍🐍🗺️

Made with :heart: by **Fardeen Ahmad Khan**
