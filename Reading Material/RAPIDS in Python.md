# RAPIDS Cheat Sheet 🚀📊

Welcome to the RAPIDS cheat sheet! RAPIDS is an open-source suite of software libraries and frameworks that enables end-to-end data science and analytics acceleration on GPUs. It is designed to be compatible with popular data science libraries and provides a seamless experience for GPU-accelerated workflows.

## Installation

You can install RAPIDS using Conda:

```bash
conda install -c rapidsai -c nvidia -c conda-forge -c defaults cuml=21.12 python=3.8 cudatoolkit=11.0
```

## Importing RAPIDS

Import RAPIDS libraries in your Python script:

```python
import cuml
import cudf
import cupy
```

## Basic Usage

### 1. Load Data with cuDF

Load and manipulate data using cuDF:

```python
import cudf

# Load CSV into cuDF DataFrame
df = cudf.read_csv('your_dataset.csv')

# Display first few rows
print(df.head())
```

### 2. GPU-Accelerated Machine Learning

Perform machine learning tasks using cuML:

```python
from cuml.ensemble import RandomForestClassifier
from cuml.model_selection import train_test_split
from cuml.metrics import accuracy_score

# Split data into train and test sets
X_train, X_test, y_train, y_test = train_test_split(df, 'target', random_state=42)

# Create and train a RandomForestClassifier
rf_classifier = RandomForestClassifier()
rf_classifier.fit(X_train, y_train)

# Make predictions
y_pred = rf_classifier.predict(X_test)

# Evaluate accuracy
accuracy = accuracy_score(y_test, y_pred)
print(f'Accuracy: {accuracy}')
```

### 3. GPU-Accelerated Data Visualization

Visualize data using cuXfilter:

```python
import cuxfilter

# Create a dashboard
dashboard = cuxfilter.Dashboards(df)

# Create charts and add to the dashboard
chart1 = cuxfilter.charts.scatter(x='column1', y='column2')
dashboard.add_charts(chart1)

# Serve the dashboard
dashboard.show()
```

## Advanced Usage

### 4. RapidsAI Notebooks

Use RAPIDS with Jupyter Notebooks:

```bash
conda install -c rapidsai -c nvidia -c conda-forge -c defaults \
  -c anaconda cuml=21.12 python=3.8 cudatoolkit=11.0 nbserverproxy jupyter
```

### 5. BlazingSQL for SQL Queries

Leverage GPU-accelerated SQL queries with BlazingSQL:

```python
from blazingsql import BlazingContext

# Create BlazingSQL context
bc = BlazingContext()

# Register a cuDF DataFrame as a table
bc.create_table('your_table', df)

# Run SQL queries on the GPU
result = bc.sql('SELECT * FROM your_table WHERE condition')
```

### 6. Follow the Author

📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and GPU-accelerated data science content.

RAPIDS accelerates your data science workflows on GPUs, providing exceptional performance for tasks ranging from data preprocessing to machine learning. Explore the power of RAPIDS! 🚀📊✨
