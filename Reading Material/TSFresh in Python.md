# TSFresh Cheat Sheet 📈📊

Welcome to the TSFresh cheat sheet! TSFresh is a powerful Python library for automatic time series feature extraction. It's a valuable tool for engineers, data scientists, and researchers working with time series data. Let's explore TSFresh with some code examples!

## Installation

You can install TSFresh using pip:

```bash
pip install tsfresh
```

## Importing TSFresh

Import TSFresh like this:

```python
from tsfresh import extract_features, select_features
from tsfresh.utilities.dataframe_functions import impute
```

## Basic Usage

### 1. Extract Features

Automatically extract features from your time series data:

```python
extracted_features = extract_features(timeseries, column_id='id', column_sort='time')
```

### 2. Impute Missing Values

Handle missing values in your extracted features:

```python
imputed_features = impute(extracted_features)
```

### 3. Select Relevant Features

Select the most relevant features for your analysis:

```python
selected_features = select_features(imputed_features, target_column)
```

## Advanced Usage

### 4. Feature Filtering

Filter features by custom criteria:

```python
from tsfresh.feature_selection import select_features

settings = tsfresh.feature_selection.from_columns(
    selected_features.drop(target_column, axis=1), 
    target_column
)
selected_features = select_features(extracted_features, settings)
```

### 5. Parallel Execution

Extract features in parallel to speed up the process:

```python
extracted_features = extract_features(
    timeseries, 
    column_id='id', 
    column_sort='time', 
    n_jobs=4  # Number of CPU cores to use
)
```

### 6. Example Time Series Data

Here's a sample structure of time series data to use with TSFresh:

```python
id, time, value
0, 1, 5
0, 2, 6
1, 1, 8
1, 2, 9
2, 1, 12
2, 2, 13
```

## Resources

- 📖 Official Documentation: [TSFresh Documentation](https://tsfresh.readthedocs.io)
- 📦 PyPI Package: [TSFresh on PyPI](https://pypi.org/project/tsfresh)
- 📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data science content.

TSFresh is a fantastic tool for feature extraction from time series data. Start utilizing its power in your time series analysis! 📈📊🧐🔥
