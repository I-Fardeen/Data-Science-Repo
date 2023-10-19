# Surprise in Python Cheat Sheet 🎁🐍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Surprise cheat sheet! Surprise is a Python library for building and analyzing recommender systems. It makes it easy to work with recommendation algorithms and evaluate their performance. Let's dive into some essential concepts and code examples.

## Installation

You can install Surprise using pip:

```bash
pip install scikit-surprise
```

## Basic Usage

### Importing Surprise

To use Surprise, you need to import it:

```python
from surprise import Dataset
from surprise import Reader
from surprise import SVD
from surprise import accuracy
from surprise.model_selection import train_test_split
```

### Creating a Dataset

You can create a dataset from your data. The data should be in the format: `user, item, rating`.

```python
# Define the reader
reader = Reader(rating_scale=(1, 5))

# Load your data
data = Dataset.load_from_df(df[['user', 'item', 'rating']], reader)
```

### Splitting Data

It's essential to split the data into training and testing sets for evaluation.

```python
trainset, testset = train_test_split(data, test_size=0.25)
```

### Building a Model

You can choose from various recommendation algorithms. Let's use SVD as an example:

```python
model = SVD()
model.fit(trainset)
```

### Making Predictions

Now you can make predictions using the trained model:

```python
predictions = model.test(testset)
```

### Model Evaluation

Evaluate the model's performance with various metrics:

```python
# Calculate RMSE (Root Mean Squared Error)
rmse = accuracy.rmse(predictions)

# Calculate MAE (Mean Absolute Error)
mae = accuracy.mae(predictions)
```

## Advanced Concepts

- **Cross-Validation**: Use cross-validation to assess the model's stability and generalization.

```python
from surprise.model_selection import cross_validate
cross_validate(model, data, measures=['RMSE', 'MAE'], cv=5, verbose=True)
```

- **Tuning Hyperparameters**: Tune the model's hyperparameters to improve performance.

- **Grid Search**: Perform a grid search to find the best combination of hyperparameters.

```python
from surprise.model_selection import GridSearchCV
param_grid = {'n_epochs': [5, 10, 15], 'lr_all': [0.002, 0.005, 0.01]}
grid_search = GridSearchCV(SVD, param_grid, measures=['RMSE', 'MAE'], cv=3)
grid_search.fit(data)
```

## Resources

📖 Official Documentation: [Surprise Documentation](https://surprise.readthedocs.io/en/stable/index.html)

Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data science-related content. Have fun building your recommender systems with Surprise! 🎁🐍🌟

Made with :heart: by **Fardeen Ahmad Khan**
