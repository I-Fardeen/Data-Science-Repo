# Dataframes using Polars in Python Cheat Sheet 🚀🐍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of Dataframes using Polars in Python! This cheat sheet will guide you through the basics of working with dataframes using the Polars library. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and Data Science insights! 🙌

## Table of Contents 🗒️

1. [Introduction to Polars](#introduction-to-polars)
2. [Installation](#installation)
3. [Creating a DataFrame](#creating-a-dataframe)
4. [Basic Operations](#basic-operations)
5. [Filtering Data](#filtering-data)
6. [Grouping and Aggregation](#grouping-and-aggregation)
7. [Merging Data](#merging-data)
8. [Handling Missing Data](#handling-missing-data)
9. [Data Visualization](#data-visualization)
10. [Resources](#resources)

## 1. Introduction to Polars 🚀

Polars is a blazingly fast DataFrame library implemented in Rust and designed for data manipulation. It provides a powerful and expressive API for data transformation and analysis.

## 2. Installation 📦

Install Polars using pip:

```bash
pip install polars
```

## 3. Creating a DataFrame 📊

Create a Polars DataFrame from a Python dictionary:

```python
import polars as pl

data = {'Name': ['Alice', 'Bob', 'Charlie'],
        'Age': [25, 30, 22]}
df = pl.DataFrame(data)
```

## 4. Basic Operations 🧮

Perform basic operations like selecting columns and rows:

```python
# Select columns
df.select(['Name', 'Age'])

# Filter rows
df.filter(df['Age'] > 25)
```

## 5. Filtering Data 🔍

Filter data based on conditions:

```python
# Filter rows where Age is greater than 25
df.filter(df['Age'] > 25)
```

## 6. Grouping and Aggregation 📊

Group data by a column and perform aggregations:

```python
# Group by 'Country' and calculate mean of 'Sales'
df.groupby('Country').agg(pl.col('Sales').mean().alias('Avg_Sales'))
```

## 7. Merging Data 🧩

Merge dataframes using different join types:

```python
# Inner join
result = dfA.join(dfB, on='Key', how='inner')
```

## 8. Handling Missing Data 🕳️

Deal with missing data using methods like `fill_none`:

```python
# Fill missing values with a default value
df.fill_none({'Age': 0})
```

## 9. Data Visualization 📈

Visualize data using Polars integration with popular plotting libraries.

## 10. Resources 📚

Explore the Polars documentation and tutorials for advanced techniques and examples:

- [Polars Documentation](https://pola-rs.github.io/polars/)
- [Polars GitHub Repository](https://github.com/pola-rs/polars)

Start working with fast and efficient dataframes in Python using Polars!

Happy data wrangling! 🚀🐍

Made with :heart: by **Fardeen Ahmad Khan**
