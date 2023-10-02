Certainly! Here's a cheat sheet in Markdown format with emojis for the "AstroPy Library in Python," along with code examples for each section:

```markdown
# AstroPy Library in Python Cheat Sheet 🌌🪐

Welcome to the cosmos of astronomy and astrophysics with AstroPy! This cheat sheet will guide you through the essential features of the AstroPy library and provide code examples for better understanding. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python insights and scientific explorations! 🌟

## Table of Contents 🗒️

1. [What is AstroPy?](#what-is-astropy)
2. [Installing AstroPy](#installing-astropy)
3. [Coordinates and Time](#coordinates-and-time)
4. [Units and Constants](#units-and-constants)
5. [FITS Files](#fits-files)
6. [Celestial Calculations](#celestial-calculations)
7. [Astronomical Tables](#astronomical-tables)
8. [Resources](#resources)

## 1. What is AstroPy? 🌌

AstroPy is an open-source Python library designed for astronomy and astrophysics. It provides tools and functions for working with celestial coordinates, time, units, constants, FITS files, and various astronomical calculations.

## 2. Installing AstroPy 🚀

Install AstroPy using pip:

```python
pip install astropy
```

## 3. Coordinates and Time ⏳

Work with celestial coordinates and time:

```python
from astropy.coordinates import EarthLocation, AltAz, get_sun, get_moon
from astropy.time import Time

location = EarthLocation(lat=28.7041, lon=77.1025)
time = Time("2023-08-31 18:00:00", scale="utc")
altaz_frame = AltAz(obstime=time, location=location)
sun = get_sun(time)
moon = get_moon(time)
```

## 4. Units and Constants 🌠

Use astronomical units and constants:

```python
from astropy import units as u
from astropy.constants import G, M_sun, R_earth

mass_sun = 1 * M_sun
gravitational_constant = G
earth_radius = R_earth.to(u.km)
```

## 5. FITS Files 📡

Read and manipulate FITS (Flexible Image Transport System) files:

```python
from astropy.io import fits

hdul = fits.open("data.fits")
data = hdul[1].data
```

## 6. Celestial Calculations 🔭

Perform various astronomical calculations:

```python
from astropy.time import Time
from astropy.coordinates import solar_system_ephemeris, EarthLocation

time = Time.now()
with solar_system_ephemeris.set("builtin"):
    jupiter = get_body("jupiter barycenter", time)
```

## 7. Astronomical Tables 📚

Access pre-defined astronomical tables:

```python
from astropy.table import Table

table = Table.read("astronomical_data.ecsv")
```

## 8. Resources 📚

Explore more about AstroPy and its applications in astronomy and astrophysics:

- [AstroPy Documentation](https://docs.astropy.org/en/stable/)
- [AstroPy GitHub Repository](https://github.com/astropy/astropy)

AstroPy is an indispensable tool for astronomers, astrophysicists, and anyone exploring the mysteries of the cosmos. It simplifies complex tasks related to astronomical calculations.

Happy stargazing and coding! 🌌🪐
