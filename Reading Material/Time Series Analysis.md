# Time Series Analysis using Python Cheat Sheet ⏰📈

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the exciting world of Time Series Analysis with Python! This cheat sheet is your comprehensive guide to mastering the art of analyzing time-dependent data. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more insights and updates! 🙌

🚀 **Getting Started with Time Series**:
To begin your journey in Time Series Analysis, make sure you have the necessary libraries installed, including NumPy, Pandas, and Matplotlib.

```bash
pip install numpy pandas matplotlib
```

💼 **Loading Time Series Data**:
Load your time series data into Python using Pandas.

```python
import pandas as pd

# Read time series data from a CSV file
df = pd.read_csv('time_series_data.csv', parse_dates=['Date'], index_col='Date')
```

📊 **Exploratory Data Analysis (EDA)**:
Perform initial data exploration to understand your time series dataset.

- **Visualize Time Series**:
```python
import matplotlib.pyplot as plt

plt.plot(df.index, df['Value'])
plt.xlabel('Date')
plt.ylabel('Value')
plt.title('Time Series Data')
plt.show()
```

- **Seasonal Decomposition**:
```python
from statsmodels.tsa.seasonal import seasonal_decompose

result = seasonal_decompose(df['Value'], model='additive')
result.plot()
plt.show()
```

📈 **Time Series Decomposition**:
Decompose your time series into its components: trend, seasonality, and residuals.

```python
from statsmodels.tsa.seasonal import seasonal_decompose

result = seasonal_decompose(df['Value'], model='additive')
trend = result.trend
seasonal = result.seasonal
residual = result.resid
```

📉 **Stationarity Testing**:
Check stationarity using methods like the Augmented Dickey-Fuller test.

```python
from statsmodels.tsa.stattools import adfuller

result = adfuller(df['Value'])
p_value = result[1]

if p_value <= 0.05:
    print("The time series is stationary.")
else:
    print("The time series is not stationary.")
```

📅 **Time Series Forecasting**:
Build forecasting models using techniques like ARIMA or Prophet.

- **ARIMA Model**:
```python
from statsmodels.tsa.arima.model import ARIMA

model = ARIMA(df['Value'], order=(1,1,1))
model_fit = model.fit()
forecast = model_fit.forecast(steps=10)
```

- **Prophet Model**:
```python
from fbprophet import Prophet

model = Prophet()
model.fit(df)
future = model.make_future_dataframe(periods=365)
forecast = model.predict(future)
```

📊 **Model Evaluation**:
Evaluate your time series forecasting models using appropriate metrics.

- **Mean Absolute Error (MAE)**:
- **Mean Squared Error (MSE)**:
- **Root Mean Squared Error (RMSE)**:
- **Mean Absolute Percentage Error (MAPE)**:

🧐 **Advanced Techniques**:
Explore advanced techniques like deep learning-based forecasting using LSTM or GRU.

Now, you're well-prepared to dive into the fascinating field of Time Series Analysis using Python. Happy analyzing! ⏰📈

Made with :heart: by **Fardeen Ahmad Khan**
