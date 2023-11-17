# PyMC3 Cheat Sheet 📝🔍

Welcome to the PyMC3 cheat sheet! PyMC3 is a powerful probabilistic programming library for Bayesian data analysis. It allows you to define probabilistic models using a high-level syntax and perform Bayesian inference. Let's dive into the key concepts and usage examples.

## Installation

You can install PyMC3 using pip:

```bash
pip install pymc3
```

## Importing PyMC3

Import PyMC3 and other necessary modules:

```python
import pymc3 as pm
import arviz as az
import numpy as np
import matplotlib.pyplot as plt
```

## Basic Concepts

### 1. Probabilistic Model

Define a simple probabilistic model:

```python
with pm.Model() as model:
    # Define prior
    theta = pm.Normal("theta", mu=0, sigma=1)

    # Define likelihood
    y = pm.Normal("y", mu=theta, sigma=1, observed=data)
```

### 2. Inference

Perform Bayesian inference using the No-U-Turn Sampler (NUTS):

```python
with model:
    trace = pm.sample(1000, tune=1000)
```

### 3. Posterior Analysis

Analyze and visualize the posterior distribution:

```python
with model:
    az.plot_posterior(trace)
    plt.show()
```

### 4. Prior Distribution

Specify and visualize the prior distribution:

```python
with model:
    prior_samples = pm.sample_prior_predictive(samples=500)
    az.plot_dist(prior_samples["theta"])
    plt.show()
```

### 5. Posterior Predictive Checks

Perform posterior predictive checks:

```python
with model:
    posterior_predictive = pm.sample_posterior_predictive(trace)
    az.plot_ppc(az.from_pymc3(posterior_predictive), data_pairs={"y": data})
    plt.show()
```

### 6. Model Comparison

Compare models using Widely Applicable Information Criterion (WAIC):

```python
with model:
    compare_dict = az.compare({"model": trace, "null": null_trace}, ic="waic")
    print(compare_dict)
```

## Advanced Usage

### 7. Hierarchical Model

Build a hierarchical model:

```python
with pm.Model() as hierarchical_model:
    # Define hyperparameters
    mu_theta = pm.Normal("mu_theta", mu=0, sigma=1)
    sigma_theta = pm.HalfNormal("sigma_theta", sigma=1)

    # Define hierarchical prior
    theta = pm.Normal("theta", mu=mu_theta, sigma=sigma_theta, shape=num_groups)

    # ... (define likelihood and perform inference)
```

### 8. Custom Likelihood

Define a custom likelihood function:

```python
def custom_likelihood(value, mu, sigma):
    # ... (custom likelihood calculation)
    return likelihood_value

with pm.Model() as custom_model:
    y = pm.DensityDist("y", custom_likelihood, observed={"value": data, "mu": mu, "sigma": sigma})
```

### 9. Gaussian Process

Implement Gaussian Process regression:

```python
with pm.Model() as gp_model:
    # Define Gaussian Process
    cov_func = pm.gp.cov.ExpQuad(1, ls=0.1)
    gp = pm.gp.Latent(cov_func=cov_func)

    # Define GP prior
    f = gp.prior("f", X=x[:, None])

    # ... (define likelihood and perform inference)
```

### 10. Follow the Author

📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and Bayesian data analysis content.

PyMC3 empowers you to perform Bayesian analysis with ease. Experiment with these examples and explore the flexibility and expressiveness of PyMC3 for your probabilistic programming needs! 📊🔍📈
