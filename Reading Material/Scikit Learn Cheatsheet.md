# Scikit-Learn (sklearn) Cheatsheet 📚

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Scikit-Learn (sklearn) Cheatsheet! This cheatsheet provides a quick reference to some of the most commonly used functions and techniques in the scikit-learn library for machine learning. 🤖

Feel free to bookmark or print this cheatsheet for your convenience. 📌

Remember to stay updated with the latest developments in the field of machine learning and scikit-learn by following the author, Fardeen Ahmad Khan, on [GitHub](https://github.com/I-Fardeen). Don't forget to give a ⭐ to show your support!

## Table of Contents 📑

1. [Installation](#installation)
2. [Importing](#importing)
3. [Data Preparation](#data-preparation)
4. [Model Selection](#model-selection)
5. [Model Training](#model-training)
6. [Model Evaluation](#model-evaluation)
7. [Hyperparameter Tuning](#hyperparameter-tuning)
8. [Saving and Loading Models](#saving-and-loading-models)

## Installation ['installation']  ⚙️

To install scikit-learn, you can use the following command:

```bash
pip install scikit-learn
```

## Importing [importing] 📥

Import the necessary modules and classes from scikit-learn:

```python
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, classification_report
from sklearn.model_selection import GridSearchCV
from sklearn.externals import joblib
```

## Data Preparation [data-preparation]: 🧬

- Load your dataset and split it into features (X) and target (y):

```python
X = dataset.drop('target', axis=1)
y = dataset['target']
```

- Split the data into training and testing sets:

```python
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

## Model Selection 🕵️‍♂️

Choose a machine learning model that suits your problem:

```python
model = LogisticRegression()
```

## Model Training 🏋️‍♂️

- Fit the model to the training data:

```python
model.fit(X_train, y_train)
```

## Model Evaluation 📊

Evaluate the trained model's performance:

```python
y_pred = model.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)
report = classification_report(y_test, y_pred)
print(f'Accuracy: {accuracy:.2f}')
print(f'Classification Report:\n{report}')
```

## Hyperparameter Tuning ⚖️

Use GridSearchCV to find the best hyperparameters:

```python
param_grid = {'C': [0.1, 1, 10], 'penalty': ['l1', 'l2']}
grid_search = GridSearchCV(LogisticRegression(), param_grid, cv=3)
grid_search.fit(X_train, y_train)
best_params = grid_search.best_params_
```

## Saving and Loading Models 💾

Save and load trained models using joblib:

```python
joblib.dump(model, 'model.pkl')
loaded_model = joblib.load('model.pkl')
```

Remember to stay updated with the latest developments in machine learning by following the author, Fardeen Ahmad Khan, on [GitHub](https://github.com/I-Fardeen). Happy learning and coding! 🚀

Made with :heart: by **Fardeen Ahmad Khan**
