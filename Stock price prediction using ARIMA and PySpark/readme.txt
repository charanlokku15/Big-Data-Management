# Stock Price Prediction with ARIMA

This project implements an ARIMA (AutoRegressive Integrated Moving Average) model for predicting AAPL stock prices using PySpark.

## Features
- Time series analysis and forecasting
- Custom ARIMA implementation
- Model evaluation metrics
- Visualization of results

## Data Preparation
1. Loaded AAPL stock price data (2017-2020)
2. Converted date format and filtered date range
3. Calculated first-order differences of closing prices
4. Removed missing values

## Exploratory Analysis
- Visualized closing price trends
- Performed Augmented Dickey-Fuller test for stationarity
- Analyzed ACF/PACF plots to identify AR/MA components

## Model Implementation
Built custom ARIMA model using PySpark:
- AR component (p=1)
- MA component (q=1)
- Implemented linear regression for coefficients
- Combined AR and MA predictions

## Evaluation
- Calculated RMSE on training data (14.16)
- Tested model on unseen data
- Visualized predictions vs actual values

## Key Steps
1. Data loading and cleaning
2. Time series decomposition
3. Stationarity testing
4. Model training
5. Prediction and evaluation

## Outputs
- Original vs predicted price plots
- Model performance metrics
- Demonstration on test dataset

## Requirements
- PySpark
- Pandas
- Matplotlib/Seaborn
- Statsmodels (for ADF test and ACF/PACF plots)

## Usage
1. Prepare your stock price data in CSV format
2. Run the data preparation steps
3. Execute the model training and evaluation cells
4. Analyze the results and visualizations

## Performance
The model achieved a training RMSE of 14.16. Test performance may vary based on market conditions.