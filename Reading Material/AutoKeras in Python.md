# AutoKeras Cheat Sheet 🤖📊

Welcome to the AutoKeras cheat sheet! AutoKeras is a powerful Python library for automated machine learning. It simplifies the process of building machine learning models by automating tasks like architecture search and hyperparameter tuning. Let's get started with some code examples!

## Installation

You can install AutoKeras using pip:

```bash
pip install autokeras
```

## Importing AutoKeras

Import AutoKeras like this:

```python
import autokeras as ak
```

## Basic Usage

### 1. Image Classification

Create a simple image classification model:

```python
clf = ak.ImageClassifier(max_trials=1)
clf.fit(x_train, y_train, epochs=10)
```

### 2. Text Classification

Build a text classification model:

```python
text_clf = ak.TextClassifier(max_trials=1)
text_clf.fit(x_text, y_text, epochs=10)
```

### 3. Structured Data Classification

Perform structured data classification:

```python
structured_clf = ak.StructuredDataClassifier(max_trials=1)
structured_clf.fit(x_structured, y_structured, epochs=10)
```

### 4. Regression

Create a regression model:

```python
regressor = ak.ImageRegressor(max_trials=1)
regressor.fit(x_train, y_train, epochs=10)
```

### 5. Structured Data Regression

Perform regression on structured data:

```python
structured_regressor = ak.StructuredDataRegressor(max_trials=1)
structured_regressor.fit(x_structured, y_structured, epochs=10)
```

## Advanced Usage

### 6. Customizing Search Space

Customize the search space for AutoKeras:

```python
clf = ak.ImageClassifier(max_trials=1, objective='val_accuracy', tuner='random')
clf.fit(x_train, y_train, epochs=10)
```

### 7. Hyperparameter Tuning

Tune hyperparameters manually:

```python
clf = ak.ImageClassifier(max_trials=1)
tuner = ak.tuners.BayesianOptimization(clf, objective='val_accuracy')
tuner.search(x_train, y_train, epochs=10)
```

## Resources

- 📖 Official Documentation: [AutoKeras Documentation](https://autokeras.com)
- 📦 PyPI Package: [AutoKeras on PyPI](https://pypi.org/project/autokeras)
- 📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and machine learning content.

AutoKeras empowers you to build machine learning models effortlessly. Explore its capabilities, automate your workflow, and enhance your machine learning journey! 🤖📊🚀
