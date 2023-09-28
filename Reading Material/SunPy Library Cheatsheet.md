# SunPy Library in Python Cheat Sheet 🌞🚀

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of solar physics with SunPy! This cheat sheet will guide you through the essentials of the SunPy library and provide code examples for better understanding. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python insights and scientific explorations! 🙌

## Table of Contents 🗒️

1. [What is SunPy?](#what-is-sunpy)
2. [Installing SunPy](#installing-sunpy)
3. [Solar Data Handling](#solar-data-handling)
4. [Coordinates and Time Handling](#coordinates-and-time-handling)
5. [Solar Observations](#solar-observations)
6. [Visualizing Solar Data](#visualizing-solar-data)
7. [Analyzing Solar Data](#analyzing-solar-data)
8. [Fits Files in SunPy](#fits-files-in-sunpy)
9. [Resources](#resources)

## 1. What is SunPy? 🌞

SunPy is a Python library for solar physics data analysis. It provides tools and functionalities for working with solar data, making it an essential resource for solar scientists and enthusiasts.

## 2. Installing SunPy 📦

Install SunPy using pip:

```python
pip install sunpy
```

## 3. Solar Data Handling 🌅

Load solar data and work with time-series data:

```python
import sunpy.data.sample
import sunpy.timeseries as ts

goes = ts.TimeSeries(sunpy.data.sample.GOES_XRS_TIMESERIES, source='XRS')
```

## 4. Coordinates and Time Handling 🌐

Work with solar coordinates and manage time effectively:

```python
import astropy.units as u
from sunpy.coordinates import frames

c = SkyCoord(0 * u.arcsec, 0 * u.arcsec, frame=frames.Helioprojective)
t = Time('2022-01-01T00:00:00')
```

## 5. Solar Observations 🔭

Access and analyze solar observations:

```python
import sunpy.map

aia_map = sunpy.map.Map(sunpy.data.sample.AIA_171_IMAGE)
aia_map.peek()
```

## 6. Visualizing Solar Data 📊

Visualize solar data using various plotting options:

```python
import sunpy.visualization.colormaps as cm
import matplotlib.pyplot as plt

aia_map.plot_settings['cmap'] = cm.get_cmap('sdoaia171')
aia_map.plot()
plt.show()
```

## 7. Analyzing Solar Data 📈

Perform scientific analysis on solar data:

```python
import sunpy.coordinates as coord
import sunpy.physics.differential_rotation as diff_rot

result = diff_rot.diff_rot(aia_map.date, frame=coord.Helioprojective)
```

## 8. Fits Files in SunPy 📄

Read and manipulate FITS files in SunPy:

```python
from sunpy.net import Fido, attrs as a
from sunpy.net import jsoc

results = Fido.search(a.Time('2022-01-01T00:00:00', '2022-01-01T01:00:00'),
                      a.Instrument('aia'), jsoc.Series('aia.lev1_euv_12s'))
```

## 9. Resources 📚

Explore more about SunPy and solar physics in Python:

- [SunPy Documentation](https://docs.sunpy.org/en/stable/index.html)
- [SunPy GitHub Repository](https://github.com/sunpy/sunpy)

Dive into the fascinating world of solar physics and unleash the power of SunPy for your solar data analysis!

Happy solar exploration and coding! 🌞🚀

Made with :heart: by **Fardeen Ahmad Khan**
