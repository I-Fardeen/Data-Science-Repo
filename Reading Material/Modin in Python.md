# Modin in Python Cheat Sheet 🚀🐼

Welcome to the Modin cheat sheet! Modin is a library that accelerates Pandas data frame operations by optimizing the use of available CPU cores. This guide will introduce you to the basics of Modin with code examples.

## Installation

You can install Modin using pip:

```bash
pip install modin
```

To enable Modin to utilize multiple CPU cores, you should also install the ray library:

```bash
pip install ray
```

## Importing Modin

To start using Modin, import it alongside Pandas:

```python
import modin.pandas as pd
```

Now, you can use Modin in place of Pandas without modifying your existing code.

## Initializing Modin

To initialize Modin with different configurations, you can use the `modin.config` module:

```python
import modin.config as mc

mc.MODIN_ENGINE = "dask"  # Use Dask as the engine

import modin.pandas as pd
```

## Reading Data

Reading data with Modin is the same as with Pandas. Just use the `read_csv` function:

```python
df = pd.read_csv("data.csv")
```

Modin will automatically parallelize data reading when available.

## Operations with Modin DataFrames

You can perform operations like filtering, group-by, and aggregations similar to Pandas:

```python
filtered_data = df[df["column"] > 5]
grouped_data = df.groupby("category").mean()
```

Modin automatically accelerates these operations by utilizing multiple CPU cores.

## Saving Data

To save data to a file, use the `to_csv` function:

```python
df.to_csv("output.csv", index=False)
```

## Switching Back to Pandas

If you ever need to switch back to Pandas, you can do so seamlessly. Just change your import statement to:

```python
import pandas as pd
```

## Resources

📖 Official Documentation: [Modin Documentation](https://modin.readthedocs.io/en/latest/)

Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data science content. Modin can significantly boost your data processing speed with minimal code changes! 🚀🐼🌟
