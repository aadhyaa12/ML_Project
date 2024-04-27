# ML_Project

# Time Series Forecasting of AAPL Stock Prices

## Dataset(s) Description
This project utilizes a dataset consisting of historical stock prices for Apple Inc. (AAPL), covering 1 year of trading [April 2023 - April 2024]. The dataset includes the following fields:

- `Date`: The trading day (typically Monday to Friday, excluding holidays).
- `Open`: The price at which the stock started trading during the business day.
- `High`: The highest price of the stock on that trading day.
- `Low`: The lowest price of the stock on that trading day.
- `Close`: The price at which the stock ended trading during the business day.
- `Adj Close`: The stock's closing price after adjustments for all applicable splits and dividend distributions.
- `Volume`: The number of shares that changed hands during the trading day.

The data was sourced from financial markets data providers and is commonly used for quantitative analysis, trading strategy development, and financial modeling. Predicting future stock prices can be crucial for investment decisions and risk management.

## Objectives
The goal is to predict the future closing prices (`Close`) of AAPL stock. Accurate predictions could be valuable for algorithmic trading, portfolio optimization, and risk assessment in production environments.

## Process Overview
The project involved an iterative approach with the following steps:
- Exploratory Data Analysis (EDA) to understand data distributions and relationships.
- Feature Engineering to create additional predictors and transform variables.
- Model Fitting, using ARIMA due to its relevance for time series forecasting.
- Model Evaluation using out-of-sample testing and error metrics like MSE.
- Diagnostic Checks to assess the adequacy of the model.

## EDA
- **X Variables**: Past stock prices (`Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`).
- **Y Variable**: Future stock price (`Close`).
- **Type of Problem**: Regression.
- **Observations**: 252 days of trading data.
- **Feature Distribution**: Examined to ensure no significant skewness that might affect the model's performance.
- **Correlation**: Analyzed to avoid multicollinearity issues.

## Feature Engineering
Discussed the necessity of transforming variables and creating new features to improve model performance. Encoding techniques and interaction features were considered.

## Model Fitting
- **Train/Test Split**: An 80/20 split was used, ensuring no leakage of information from the test set into the training process.
- **Model Choice**: The ARIMA model was chosen for its ability to handle time series data and provide interpretable parameters.

## Validation / Metrics
- **Primary Metric**: Mean Squared Error (MSE) was chosen due to its relevance for continuous outcomes.
- **Model Weaknesses**: The limitations of ARIMA, including the assumption of linearity and the difficulty in capturing complex patterns, were acknowledged.

## Production Advice
Recommendations for deploying the model in a production setting are provided, with precautions to avoid overfitting and to ensure continuous monitoring for performance decay.

## Going Further
Suggestions to enhance the model include incorporating more granular data, considering additional external factors, and employing more complex models such as machine learning algorithms.

## Visual Data Insights

Here we include various visual representations that serve as key insights into the dataset and the performance of our forecasting model.

## Distribution Visualization of Trading Metrics
 ![Distribution of Stock Trading Metrics](https://github.com/aadhyaa12/ML_Project/blob/main/WhatsApp%20Image%202024-04-26%20at%209.35.54%20PM-2.jpeg?raw=true)")

This collection of histograms with superimposed Kernel Density Estimates illustrates the diverse range of trading metrics for AAPL, such as opening, closing, high, low prices, and volume over the past year. Noticeable is the trading volume's bimodality, suggesting inconsistent trading activity levels.

## Statistical Dispersion of Stock Metrics
![Box Plot Analysis of Stock Prices](https://github.com/aadhyaa12/ML_Project/blob/main/WhatsApp%20Image%202024-04-26%20at%209.35.54%20PM-3.jpeg?raw=true")

Box plot representations for AAPL's trading metrics provide a succinct statistical summary, including median, quartiles, and outliers, especially highlighting days with atypical trading volumes.

## Predictive Modeling
 ![Initial Stock Price Prediction](https://github.com/aadhyaa12/ML_Project/blob/main/WhatsApp%20Image%202024-04-26%20at%209.35.54%20PM-4.jpeg?raw=true")

The line chart contrasts the early model predictions against actual stock prices, revealing the initial phase of the model's ability to grasp general trends but not volatility.

## Predictive Modeling
 ![Stock Price Prediction with Poor Fit](https://github.com/aadhyaa12/ML_Project/blob/main/WhatsApp%20Image%202024-04-26%20at%209.35.54%20PM-5.jpeg?raw=true")
 
Here, a clear discrepancy is shown between the model's predictions and the actual stock prices, underscoring the complexities in modeling stock price behaviors.

## Yearly Trend of AAPL's Closing Prices
 ![Historical Trend of Closing Prices](https://github.com/aadhyaa12/ML_Project/blob/main/WhatsApp%20Image%202024-04-26%20at%209.35.54%20PM-6.jpeg?raw=true)")
 
A time series representation that charts the fluctuation in AAPL's closing prices over the year, laying the groundwork for the predictive modeling.

## Predictive Confidence Analysis
 ![Model Prediction with Confidence Interval](https://github.com/aadhyaa12/ML_Project/blob/main/WhatsApp%20Image%202024-04-26%20at%209.35.54%20PM-7.jpeg?raw=true")

This prediction plot, inclusive of actual prices, features a confidence interval indicative of the model's certainty levels.

## Learning Curve of the Model
![Model Training and Testing Loss](https://github.com/aadhyaa12/ML_Project/blob/main/WhatsApp%20Image%202024-04-26%20at%209.35.54%20PM-8.jpeg?raw=true")

This curve delineates the evolution of model loss during the training process, illustrating how well the model is learning from the data.

## Comprehensive Predictive Performance
![Comprehensive Stock Price Prediction](https://github.com/aadhyaa12/ML_Project/blob/main/WhatsApp%20Image%202024-04-26%20at%209.35.54%20PM-9.jpeg?raw=true")

A detailed chart showing the actual versus predicted prices, this image illustrates the efficacy of the model on both the training and testing sets.

## Technical Analysis
 ![Stock Prices and Moving Average](https://github.com/aadhyaa12/ML_Project/blob/main/WhatsApp%20Image%202024-04-26%20at%209.35.54%20PM.jpeg?raw=true")

Comparing AAPL's actual closing prices with a 50-day moving average, this graph demonstrates one of the many technical tools used in stock analysis.

## Longitudinal Analysis of Closing Prices
![Trend Analysis of AAPL Closing Prices](https://github.com/aadhyaa12/ML_Project/blob/main/WhatsApp%20Image%202024-04-26%20at%209.35.53%20PM.jpeg?raw=true")

A specialized focus on the closing price trend, this graph offers a direct view into the stock's price progression over time, and acts as a benchmark for forecasting performance.

---
*End of README.md*
"""
