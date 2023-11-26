# 🏠 Capstone Project: House Price Prediction

Welcome to the **House Price Prediction Capstone Project** repository on GitHub! 🎉 In this project, we invite you to explore the exciting world of data analysis, prediction modeling, and feature engineering in the context of real estate. Whether you're an aspiring data scientist or a curious learner, this project is designed to provide valuable insights into predicting house prices using a variety of techniques and tools.

Made with :heart: by **Fardeen Ahmad Khan and Team (attributions in the code file)**

## Project Overview 🌟

This capstone project is dedicated to unraveling the dynamics of house prices, offering an insightful journey through data cleaning, exploratory data analysis, modeling, and feature engineering. By diving into this project, you will:
- Gain hands-on experience in cleaning and preparing real-world datasets for analysis.
- Explore the distribution and relationships of various factors influencing house prices.
- Develop predictive models using multiple regression algorithms, including Linear Regression, Decision Tree Regression, Random Forest Regression, KNN Regression, and ANN Regression.
- Enhance model performance through feature engineering techniques.
- Fine-tune model hyperparameters for optimal predictions.
- Utilize a Light Gradient Boosting Algorithm for further accuracy improvement.

We're thrilled to have you on this learning journey, and we hope you find this capstone project engaging and educational. Let's get started and uncover the insights that lie within the data! 🚀

## Project Contents 📁

This project is organized into the following sections:
- Data Cleaning: Prepare the dataset by addressing outliers, handling null values, and transforming variables.
- Data Analysis: Dive into the distribution and relationships of different variables through univariate and bivariate analysis.
- Hypothesis Testing: Validate assumptions and extract meaningful insights from the data.
- Data Modeling: Apply a variety of regression algorithms to predict house prices and improve model performance through boosting techniques.
- Feature Engineering: Enhance the predictive power of models by engineering new features.
- Model Tuning: Optimize model performance through hyperparameter tuning.

Feel free to explore each section in detail and engage with the provided code and analyses. Happy learning!


## Data Cleaning 🧹
- Create new columns for Year, Month, and Date from dayhours in the dataset.
- Identify and address outliers, handle null values, and remove irrelevant data points.
- Remove rows with $ values in the year_built column and NaN values in living and lot measures.
- Address values like 0.5 and 0.7 for room_bath using appropriate treatment.
- Handle null and $ values in the ceil or number of floors in a house column, replacing them with 2.
- Convert Zipcode to City Name for better interpretability.
- Create scaled data with encoded city values for modeling.

## Data Analysis 📊

### Univariate Analysis 1️⃣
- Perform univariate analysis on different variables to understand their distributions and characteristics.
- Analyze the distribution of housing prices.
- Investigate the distribution of bedrooms, bathrooms, living measures, lot measures, number of floors, coast presence, sight status, condition, quality, year built, and location (city).

### Bivariate Analysis 2️⃣
- Conduct correlation analysis to explore relationships between different variables.
- Create scatter plots to visualize relationships between housing prices and each individual variable.

### Hypothesis Testing 🔬
- Perform hypothesis testing to validate assumptions and draw meaningful insights from the data.

## Data Modeling 🛠️
- Apply various regression algorithms to predict house prices.
- Utilize Linear Regression, Decision Tree Regression, Random Forest Regression, KNN Regression, and ANN Regression.
- Implement boosting algorithms to improve model performance.

## Feature Engineering 🔍
- Enhance the predictive power of the models through feature engineering techniques.

## Model Tuning ⚙️
- Perform hyperparameter tuning to optimize model performance.
- Apply tuned parameters to a Light Gradient Boosting Algorithm for improved accuracy.

Made with :heart: by **Fardeen Ahmad Khan and Team**
