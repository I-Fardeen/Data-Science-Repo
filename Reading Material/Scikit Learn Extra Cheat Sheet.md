# Scikit-learn-extra in Python Cheat Sheet 🧬🐍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Scikit-learn-extra cheat sheet! Scikit-learn-extra is a Python library that extends the capabilities of the popular Scikit-learn library. It provides additional tools and algorithms for machine learning. Let's explore Scikit-learn-extra with some code examples.

## Installation

You can install Scikit-learn-extra using pip:

```bash
pip install scikit-learn-extra
```

## Importing Scikit-learn-extra

To start using Scikit-learn-extra, import it:

```python
from sklearn_extra.cluster import KMedoids
```

## K-Medoids Clustering

Use the K-Medoids clustering algorithm:

```python
# Create a KMedoids instance
kmedoids = KMedoids(n_clusters=3, random_state=0)

# Fit the model
kmedoids.fit(X)
```

## Neighborhood Components Analysis (NCA)

Perform neighborhood components analysis for feature selection:

```python
from sklearn_extra.feature_selection import NCA

# Create an NCA instance
nca = NCA(max_iter=100, tol=1e-4)

# Fit the model
nca.fit(X, y)
```

## TimeSeriesSplit

Use TimeSeriesSplit for time series cross-validation:

```python
from sklearn_extra.model_selection import TimeSeriesSplit

# Create TimeSeriesSplit
tscv = TimeSeriesSplit(n_splits=5)

# Use it in cross-validation
for train_index, test_index in tscv.split(X):
    X_train, X_test = X[train_index], X[test_index]
```

## Resources

📖 Official Documentation: [Scikit-learn-extra Documentation](https://scikit-learn-extra.readthedocs.io/en/latest/index.html)

Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data science content. Scikit-learn-extra adds extra power to your machine learning toolbox! 🧬🐍🔍📊

Made with :heart: by **Fardeen Ahmad Khan**
