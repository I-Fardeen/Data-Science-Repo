# PyMC Library in Python Cheat Sheet 📊🔍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of Bayesian statistics and probabilistic programming with PyMC! This cheat sheet will guide you through the essential features of the PyMC library and provide code examples for better understanding. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python insights and Bayesian exploration! 🌟

## Table of Contents 🗒️

1. [What is PyMC?](#what-is-pymc)
2. [Installing PyMC](#installing-pymc)
3. [Defining Probabilistic Models](#defining-probabilistic-models)
4. [Inference with Markov Chain Monte Carlo (MCMC)](#inference-with-mcmc)
5. [Model Visualization](#model-visualization)
6. [Posterior Analysis](#posterior-analysis)
7. [Advanced Features](#advanced-features)
8. [Resources](#resources)

## 1. What is PyMC? 📊

PyMC is an open-source probabilistic programming framework in Python. It allows you to build and analyze complex probabilistic models using Bayesian statistics.

## 2. Installing PyMC 🚀

Install PyMC using pip:

```python
pip install pymc3
```

## 3. Defining Probabilistic Models 🔍

Define your probabilistic model using Python syntax:

```python
import pymc3 as pm

with pm.Model() as model:
    # Define priors
    parameter = pm.Normal("parameter", mu=0, sigma=1)

    # Define likelihood
    data = pm.Normal("data", mu=parameter, sigma=1, observed=data_observed)
```

## 4. Inference with Markov Chain Monte Carlo (MCMC) 🔄

Perform Bayesian inference with MCMC sampling:

```python
with model:
    trace = pm.sample(1000)
```

## 5. Model Visualization 📈

Visualize your probabilistic model:

```python
pm.traceplot(trace)
```

## 6. Posterior Analysis 📉

Analyze posterior distributions:

```python
pm.summary(trace)
pm.plot_posterior(trace)
```

## 7. Advanced Features 🧮

Explore advanced features like hierarchical models, GLM, and more:

```python
# Hierarchical model
with pm.Model():
    group_mean = pm.Normal("group_mean", mu=0, sigma=1)
    group_std = pm.HalfNormal("group_std", sigma=1)
    individual = pm.Normal("individual", mu=group_mean, sigma=group_std, observed=data)

# Generalized Linear Model (GLM)
with pm.Model():
    pm.GLM.from_formula("y ~ x", data)
```

## 8. Resources 📚

Learn more about PyMC and Bayesian statistics:

- [PyMC Documentation](https://docs.pymc.io/)
- [PyMC GitHub Repository](https://github.com/pymc-devs/pymc3)

PyMC is a powerful tool for Bayesian data analysis and probabilistic modeling in Python.

Enjoy exploring the world of Bayesian statistics with PyMC! 📊🔍
