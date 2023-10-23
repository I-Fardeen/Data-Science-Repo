# CartoPy in Python Cheat Sheet 🌍🗺️

Made wtih :heart: by **Fardeen Ahmad Khan**

Welcome to the CartoPy cheat sheet! CartoPy is a Python library for cartographic projections and geospatial data visualization. It makes it easier to create maps, plot geospatial data, and apply various projections in Python. Let's explore the key concepts and code examples for CartoPy.

## Installation

You can install CartoPy using pip:

```bash
pip install cartopy
```

## Importing CartoPy

To get started with CartoPy, import the library:

```python
import cartopy.crs as ccrs
import cartopy.feature as cfeature
```

## Creating a Geographic Plot

You can create a geographic plot with CartoPy by specifying the projection and adding features:

```python
import matplotlib.pyplot as plt

# Create a GeoAxes with a PlateCarree projection
ax = plt.axes(projection=ccrs.PlateCarree())

# Add coastlines and borders
ax.add_feature(cfeature.COASTLINE)
ax.add_feature(cfeature.BORDERS, linestyle=':')
```

## Plotting Points on a Map

Plot geospatial data points on the map using CartoPy:

```python
import matplotlib.pyplot as plt

# Create a GeoAxes with a Mercator projection
ax = plt.axes(projection=ccrs.Mercator())

# Plot latitude and longitude points
ax.plot(lon, lat, marker='o', markersize=5, color='red', transform=ccrs.PlateCarree())
```

## Applying Projections

CartoPy supports various map projections, such as Lambert Conformal, Orthographic, and more:

```python
ax = plt.axes(projection=ccrs.LambertConformal())

ax = plt.axes(projection=ccrs.Orthographic(central_longitude=0, central_latitude=0))
```

## Resources

📖 Official Documentation: [CartoPy Documentation](https://scitools.org.uk/cartopy/docs/latest/)

Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and geospatial data visualization content. Dive into the world of cartographic projections with CartoPy! 🌍🗺️🌟

Made wtih :heart: by **Fardeen Ahmad Khan**
