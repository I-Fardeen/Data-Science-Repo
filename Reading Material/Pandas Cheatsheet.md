Feel free to share this with others and don't forget to star the repo for more content.  
Made with ❤️ Fardeen Ahmad Khan

# 🐼 Pandas Cheatsheet 🐼

Pandas is a powerful library for data manipulation and analysis in Python. It provides data structures and functions needed to work with structured data efficiently.

## Import Pandas 📚

```python
import pandas as pd
```

## Data Structures 🧱

### Series 📈

A one-dimensional labeled array.

```python
data = pd.Series([1, 2, 3])
```

### DataFrame 📊

A two-dimensional labeled data structure with columns.

```python
data = {'Column1': [1, 2, 3], 'Column2': ['A', 'B', 'C']}
df = pd.DataFrame(data)
```

## Reading Data 📖

### CSV 📄

```python
df = pd.read_csv('data.csv')
```

### Excel 📊

```python
df = pd.read_excel('data.xlsx')
```

## Data Exploration 🔍

### Basic Information 📋

```python
df.head()        # Display the first n rows
df.info()        # Summary of dataframe
df.shape         # Number of rows and columns
df.columns       # List of column names
df.dtypes        # Data types of columns
```

### Summary Statistics 📊

```python
df.describe()    # Descriptive statistics
df.mean()        # Mean of columns
df.corr()        # Correlation matrix
```

## Data Selection 🔍

### Indexing and Slicing 🔗

```python
df['Column1']         # Select one column
df[['Column1', 'Column2']]  # Select multiple columns
df.iloc[0]            # Select row by index
df.iloc[0:3]          # Select rows by index range
```

### Filtering 🔍

```python
df[df['Column1'] > 2]       # Filter rows
df[(df['Column1'] > 2) & (df['Column2'] == 'B')]  # Multiple conditions
```

## Data Manipulation 🛠️

### Adding Columns ➕

```python
df['NewColumn'] = values
```

### Renaming Columns 🔄

```python
df.rename(columns={'OldName': 'NewName'}, inplace=True)
```

### Aggregation 📊

```python
df.groupby('Column').mean()
```

### Sorting 🔀

```python
df.sort_values(by='Column')
```

### Handling Missing Data 🚫

```python
df.dropna()          # Drop rows with NaN values
df.fillna(value)     # Fill NaN values
```

## Data Visualization 📊

### Plotting 📈

```python
df.plot(x='Column1', y='Column2', kind='scatter')
df['Column'].plot(kind='hist')
```

## Data I/O 📥📤

### CSV 📄

```python
df.to_csv('output.csv', index=False)
```

### Excel 📊

```python
df.to_excel('output.xlsx', index=False)
```

## More Resources 📚

- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Pandas User Guide](https://pandas.pydata.org/docs/user_guide/index.html)
- [10 Minutes to Pandas](https://pandas.pydata.org/docs/getting_started/10min.html)

Made with ❤️ Fardeen Ahmad Khan
