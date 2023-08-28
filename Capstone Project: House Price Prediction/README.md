# Capstone Project: House Price Prediction

## Data Cleaning
- Create new columns for Year, Month, and Date from dayhours in the dataset.
- Identify and address outliers, handle null values, and remove irrelevant data points.
- Remove rows with $ values in the year_built column and NaN values in living and lot measures.
- Address values like 0.5 and 0.7 for room_bath using appropriate treatment.
- Handle null and $ values in the ceil or number of floors in a house column, replacing them with 2.
- Convert Zipcode to City Name for better interpretability.
- Create scaled data with encoded city values for modeling.

## Data Analysis
### Univariate Analysis
- Perform univariate analysis on different variables to understand their distributions and characteristics.
- Analyze the distribution of housing prices.
- Investigate the distribution of bedrooms, bathrooms, living measures, lot measures, number of floors, coast presence, sight status, condition, quality, year built, and location (city).

### Bivariate Analysis
- Conduct correlation analysis to explore relationships between different variables.
- Create scatter plots to visualize relationships between housing prices and each individual variable.

### Hypothesis Testing
- Perform hypothesis testing to validate assumptions and draw meaningful insights from the data.

## Data Modeling
- Apply various regression algorithms to predict house prices.
- Utilize Linear Regression, Decision Tree Regression, Random Forest Regression, KNN Regression, and ANN Regression.
- Implement boosting algorithms to improve model performance.

## Model Tuning
- Perform hyperparameter tuning to optimize model performance.
- Apply tuned parameters to a Light Gradient Boosting Algorithm for improved accuracy.

## Feature Engineering
- Enhance the predictive power of the models through feature engineering techniques.
