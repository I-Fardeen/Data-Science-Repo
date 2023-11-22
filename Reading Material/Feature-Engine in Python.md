# Feature-Engine in Python Cheat Sheet 🚀🐍

Welcome to the Feature-Engine in Python cheat sheet! Feature-Engine is a powerful library for feature engineering, providing a variety of tools to preprocess and transform your data. Whether you're dealing with missing values, encoding categorical variables, or scaling features, this cheat sheet will guide you through essential concepts and examples.

## Installation

Install Feature-Engine using pip:

```bash
pip install feature-engine
```

## Importing Feature-Engine

Import Feature-Engine in your Python script or Jupyter notebook:

```python
from feature_engine import preprocessing as pp
```

## Basic Concepts

### 1. Handling Missing Data

Impute missing values using various strategies:

```python
# Impute missing values with mean
imputer = pp.MeanMedianImputer(imputation_method='mean')
df['your_column'] = imputer.fit_transform(df[['your_column']])
```

### 2. Encoding Categorical Variables

Encode categorical variables with one-hot encoding or ordinal encoding:

```python
# One-hot encoding
encoder = pp.OneHotEncoder(variables=['categorical_column'])
df_encoded = encoder.fit_transform(df)

# Ordinal encoding
encoder = pp.OrdinalEncoder(encoding_method='arbitrary', variables=['ordinal_column'])
df_encoded = encoder.fit_transform(df)
```

### 3. Scaling Features

Scale numerical features:

```python
# MinMax scaling
scaler = pp.MinMaxScaler()
df_scaled = scaler.fit_transform(df[['numerical_column']])
```

### 4. Discretization

Discretize numerical variables:

```python
# Equal-width discretization
disc = pp.EqualWidthDiscretiser(bins=5, variables=['numerical_column'])
df_discrete = disc.fit_transform(df)
```

### 5. Outlier Handling

Handle outliers with capping or trimming:

```python
# Capping outliers
capper = pp.OutlierTrimmer(capping_method='iqr', tail='right', fold=1.5, variables=['numerical_column'])
df_no_outliers = capper.fit_transform(df)
```

### 6. Feature Creation

Create new features:

```python
# Mathematical combination
fe = pp.CombineWithReferenceFeature(variables_to_combine=['var1', 'var2'], reference_variables=['ref1', 'ref2'], method='add')
df_combined = fe.fit_transform(df)
```

## Advanced Usage

### 7. Feature Extraction

Extract information from features:

```python
# Extract datetime features
extractor = pp.DateVariableTransformer(variables=['date_column'], date_format='%Y-%m-%d')
df_extracted = extractor.fit_transform(df)
```

### 8. Custom Transformers

Create and use custom transformers:

```python
from sklearn.base import BaseEstimator, TransformerMixin

class CustomTransformer(BaseEstimator, TransformerMixin):
    def fit(self, X, y=None):
        return self
    
    def transform(self, X):
        # Your custom transformation logic
        return X

# Use the custom transformer
custom_transformer = CustomTransformer()
df_transformed = custom_transformer.fit_transform(df)
```

### 9. Follow the Author

📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and machine learning-related content.

Dive into the world of feature engineering with Feature-Engine in Python! 🛠️🔍💡
