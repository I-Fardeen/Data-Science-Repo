# Orange Cheat Sheet 🍊🐍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Orange cheat sheet! Orange is a versatile Python library that simplifies machine learning and data visualization. It's a powerful tool for data exploration and predictive modeling. Let's explore Orange with some code examples!

## Installation

You can install Orange using pip:

```bash
pip install orange3
```

## Importing Orange

Import Orange like this:

```python
import Orange
```

## Basic Usage

### 1. Loading Data

Load your dataset (CSV, Excel, or other formats) using Orange:

```python
data = Orange.data.Table('your_dataset.csv')
```

### 2. Data Exploration

Perform basic data exploration:

```python
data.domain
len(data)
data[0]
```

### 3. Data Visualization

Visualize your data using Orange's data visualization tools:

```python
box_plot = Orange.widgets.visualize.PyBoxPlot(data)
box_plot.show()
```

## Data Preprocessing

### 4. Data Preprocessing

Orange provides tools for data preprocessing, including normalization and feature selection:

```python
from Orange.preprocess import Normalize
normalized_data = Normalize()(data)
```

### 5. Feature Selection

Select the most relevant features for your analysis:

```python
from Orange.preprocess import SelectBestFeatures
selected_data = SelectBestFeatures()(data)
```

## Building Models

### 6. Model Building

Build machine learning models with Orange:

```python
from Orange.classification import TreeLearner

tree_classifier = TreeLearner()
tree_classifier = tree_classifier(data)
```

### 7. Model Evaluation

Evaluate model performance with Orange's evaluation tools:

```python
from Orange.evaluation import CrossValidation
results = CrossValidation(data, [tree_classifier])
```

## Advanced Usage

### 8. Data Mining

Use Orange for more advanced data mining tasks like clustering and association rule mining:

```python
from Orange.clustering import hierarchical

clusterer = hierarchical.HierarchicalClustering()
hierarchical_clustering = clusterer(data)
```

### 9. Machine Learning Pipelines

Create machine learning pipelines with Orange:

```python
from Orange.preprocess import AddClassifier

learner = Orange.classification.SVMLearner()
learner = learner(data)

pipeline = learner | AddClassifier(TreeLearner())
pipeline = pipeline(data)
```

## Resources

- 📖 Official Documentation: [Orange Documentation](https://orange.biolab.si/documentation/)
- 📦 PyPI Package: [Orange on PyPI](https://pypi.org/project/orange3/)
- 📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data science content.

Orange is a powerful tool for data analysis and machine learning. Start exploring and analyzing your data with ease! 🍊🐍📊🤖

Made with :heart: by **Fardeen Ahmad Khan**
