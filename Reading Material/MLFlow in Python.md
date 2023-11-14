# MLFlow Cheat Sheet 🚀📊

Welcome to the MLFlow cheat sheet! MLFlow is an open-source platform for managing the end-to-end machine learning lifecycle. It helps you track experiments, package code into reproducible runs, and share/publish models across different tools.

## Installation

You can install MLFlow using pip:

```bash
pip install mlflow
```

## Importing MLFlow

Import MLFlow in your Python script:

```python
import mlflow
```

## Basic Usage

### 1. Tracking Experiments

Initialize an experiment and log parameters, metrics, and artifacts:

```python
import mlflow

# Start experiment
with mlflow.start_run():
    # Log parameters
    mlflow.log_param("param_name", param_value)
    
    # Log metrics
    mlflow.log_metric("metric_name", metric_value)
    
    # Log artifacts (files)
    mlflow.log_artifact("file_path")
```

### 2. Logging Models

Log your machine learning model:

```python
import mlflow.sklearn

# Train a model
with mlflow.start_run():
    model = train_model()
    
    # Log the model
    mlflow.sklearn.log_model(model, "model_name")
```

### 3. Running Projects

Run your machine learning project:

```bash
mlflow run your_project_directory -P param_name=param_value
```

## Advanced Usage

### 4. Experiment Tracking UI

Launch the MLFlow UI to visualize experiments:

```bash
mlflow ui
```

Visit `http://localhost:5000` in your browser.

### 5. Managing Environments

Create and manage Conda environments for your projects:

```bash
mlflow run --no-conda your_project_directory
mlflow run --use-conda your_project_directory
```

### 6. Serving Models

Serve your ML model as a REST API:

```bash
mlflow models serve -m model_path
```

## Resources

- 📖 Official Documentation: [MLFlow Documentation](https://www.mlflow.org/docs/latest/index.html)
- 📦 PyPI Package: [MLFlow on PyPI](https://pypi.org/project/mlflow/)
- 📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and machine learning content.

MLFlow provides an organized and efficient way to manage your machine learning projects. Track, reproduce, and deploy models seamlessly with MLFlow! 🚀📊✨
