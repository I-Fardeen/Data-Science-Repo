# Polars Library in Python Cheat Sheet 🐻📊

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of Polars Library in Python! This cheat sheet will guide you through the essential aspects of using Polars for data manipulation and analysis. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and Data Science insights! 🙌

## Table of Contents 🗒️

1. [Introduction to Polars](#introduction-to-polars)
2. [Installing Polars](#installing-polars)
3. [Creating DataFrames](#creating-dataframes)
4. [Basic Operations](#basic-operations)
5. [Filtering Data](#filtering-data)
6. [Aggregating Data](#aggregating-data)
7. [Joining DataFrames](#joining-dataframes)
8. [Grouping and Pivot](#grouping-and-pivot)
9. [Data Visualization](#data-visualization)
10. [Exporting Data](#exporting-data)

## 1. Introduction to Polars 🐼

Polars is a fast DataFrame library implemented in Rust and built for data manipulation tasks in Python. It's designed to be efficient and easy to use, making it a powerful tool for working with tabular data.

## 2. Installing Polars 🛠️

You can install Polars using pip:

```bash
pip install polars
```

## 3. Creating DataFrames 📊

Create DataFrames from various data sources, including CSV files, Parquet files, and more. For example:

```python
import polars as pl

# Create a DataFrame from a CSV file
df = pl.read_csv("data.csv")
```

## 4. Basic Operations ✨

Perform basic DataFrame operations like selecting columns, renaming columns, and calculating descriptive statistics. For example:

```python
# Select columns
selected_df = df.select(["column1", "column2"])

# Rename columns
df = df.with_column_renamed({"old_name": "new_name"})

# Calculate mean
mean_value = df["column"].mean()
```

## 5. Filtering Data 🔍

Filter and subset data based on specific conditions using Polars. For example:

```python
# Filter rows where column value is greater than 10
filtered_df = df.filter(df["column"] > 10)
```

## 6. Aggregating Data 📈

Aggregate data using functions like `groupby`, `agg`, and `pivot` for summarizing and analyzing information. For example:

```python
# Group by a column and calculate mean
grouped_df = df.groupby("category").agg(pl.col("value").mean())

# Pivot table
pivot_df = df.pivot("row_column", "column_column", "value_column")
```

## 7. Joining DataFrames 🤝

Combine DataFrames through different types of joins (inner, outer, left, right) to merge data. For example:

```python
# Inner join
joined_df = df1.inner_join(df2, on="key_column")
```

## 8. Grouping and Pivot 🧮

Group data by one or more columns and pivot tables for cross-tabulation. For example:

```python
# Group by multiple columns
grouped_df = df.groupby(["column1", "column2"])

# Pivot table
pivot_df = df.pivot("row_column", "column_column", "value_column")
```

## 9. Data Visualization 📊

Visualize your data using libraries like Matplotlib or Seaborn, seamlessly integrating with Polars DataFrames. For example:

```python
import matplotlib.pyplot as plt

# Plot data
plt.plot(df["x_column"], df["y_column"])
plt.xlabel("X")
plt.ylabel("Y")
plt.show()
```

## 10. Exporting Data 💾

Save your processed data back to various file formats, including CSV, Parquet, and more. For example:

```python
# Export to CSV
df.write_csv("output.csv")
```

Explore Polars, and discover how it can streamline your data manipulation tasks efficiently!

Happy coding with Polars! 🐻📊

Made with :heart: by **Fardeen Ahmad Khan**
