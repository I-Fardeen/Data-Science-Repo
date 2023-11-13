# TPOT Cheat Sheet 🧬📊

Welcome to the TPOT cheat sheet! TPOT is an automated machine learning library in Python that helps you optimize machine learning pipelines. It efficiently explores a wide range of models and hyperparameters to find the best combination for your dataset. Let's dive into the essentials with some code examples!

## Installation

You can install TPOT using pip:

```bash
pip install tpot
```

## Importing TPOT

Import TPOT like this:

```python
from tpot import TPOTClassifier, TPOTRegressor
```

## Basic Usage

### 1. Classification

Automate the classification pipeline:

```python
clf = TPOTClassifier(generations=5, population_size=20, random_state=42, verbosity=2)
clf.fit(x_train, y_train)
```

### 2. Regression

Optimize regression pipeline:

```python
regressor = TPOTRegressor(generations=5, population_size=20, random_state=42, verbosity=2)
regressor.fit(x_train, y_train)
```

## Advanced Usage

### 3. Customizing Search Space

Customize the search space for TPOT:

```python
custom_tpot = TPOTClassifier(
    generations=5,
    population_size=20,
    config_dict='TPOT sparse',
    random_state=42,
    verbosity=2
)
custom_tpot.fit(x_train, y_train)
```

### 4. Scoring Metrics

Specify custom scoring metrics:

```python
custom_metrics = TPOTClassifier(
    generations=5,
    population_size=20,
    scoring='accuracy',
    random_state=42,
    verbosity=2
)
custom_metrics.fit(x_train, y_train)
```

### 5. Feature Preprocessing

Include feature preprocessing in the pipeline:

```python
with_preprocessing = TPOTClassifier(
    generations=5,
    population_size=20,
    config_dict='TPOT light',
    preprocessing=('standardize', 'pca', 'white', 'fast_ica', 'kernel_pca'),
    random_state=42,
    verbosity=2
)
with_preprocessing.fit(x_train, y_train)
```

## Resources

- 📖 Official Documentation: [TPOT Documentation](http://epistasislab.github.io/tpot/)
- 📦 PyPI Package: [TPOT on PyPI](https://pypi.org/project/tpot/)
- 📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and machine learning content.

TPOT simplifies the process of optimizing your machine learning pipelines. Dive into its features, streamline your workflow, and enjoy automated model optimization! 🧬📊🚀
