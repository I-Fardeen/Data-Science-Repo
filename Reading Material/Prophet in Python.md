# Prophet in Python Cheat Sheet 📈🔮

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Prophet cheat sheet! Prophet is an open-source forecasting tool developed by Facebook. It is designed for forecasting time series data, making it a valuable tool for analysts and data scientists. Let's dive into Prophet with some code examples.

## Installation

You can install Prophet using pip:

```bash
pip install pystan==2.19.1.1
pip install fbprophet
```

## Importing Prophet

To start using Prophet, import it as follows:

```python
from fbprophet import Prophet
```

## Basic Usage

Prophet expects a DataFrame with two columns: `ds` (the date or time) and `y` (the value you want to forecast). Here's how to use it:

```python
import pandas as pd

# Create a DataFrame
df = pd.DataFrame({
  'ds': ['2023-01-01', '2023-01-02', '2023-01-03'],
  'y': [10, 15, 12]
})

# Initialize the model
model = Prophet()

# Fit the model to your data
model.fit(df)

# Create a future DataFrame
future = model.make_future_dataframe(periods=365)

# Make predictions
forecast = model.predict(future)

# Plot the forecast
fig = model.plot(forecast)
```

## Custom Seasonality

You can add custom seasonalities to your model. For example, to add daily seasonality:

```python
model.add_seasonality(
    name='daily',
    period=1,
    fourier_order=3
)
```

## Resources

- 📖 Official Documentation: [Prophet Documentation](https://facebook.github.io/prophet/)
- 📦 PyPI Package: [Prophet on PyPI](https://pypi.org/project/fbprophet/)
- 📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data science content.

Prophet simplifies time series forecasting, making it accessible for everyone. 📈🔮✨

Made with :heart: by **Fardeen Ahmad Khan**
