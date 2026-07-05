# Yes Bank OHLC Data Analysis

This project analyzes Yes Bank historical OHLC stock price data and builds a machine learning regression model to predict the closing price.

## Project Overview

The dataset contains monthly stock price records of Yes Bank with the following columns:

- `Date`: Month and year of the stock price record
- `Open`: Opening stock price
- `High`: Highest stock price during the period
- `Low`: Lowest stock price during the period
- `Close`: Closing stock price, used as the target variable

The main goal of this project is to understand stock price movement, volatility, outliers, and relationships between OHLC variables, then use these insights to build a predictive model for the closing price.

## Business Problem

Investors and analysts need to understand how Yes Bank stock has moved over time and whether historical price features can help estimate the closing price. This project helps identify trends, risky periods, volatility, and useful features for stock price prediction.

## Steps Performed

1. Loaded and understood the dataset
2. Checked missing values and duplicate records
3. Performed exploratory data analysis using charts
4. Analyzed stock trends, volatility, returns, and outliers
5. Converted date into `Year` and `Month` features
6. Handled outliers using log transformation
7. Scaled the input features
8. Built and compared regression models
9. Selected the final model based on evaluation metrics

## Models Used

- Linear Regression
- Ridge Regression
- Random Forest Regressor

Linear Regression was selected as the final model because it gave a very high R2 Score with low error values and is simple to interpret.

## Evaluation Metrics

The models were evaluated using:

- MAE
- MSE
- RMSE
- R2 Score

R2 Score was considered the main metric because it shows how well the model explains the variation in the closing price.

## Final Model

The final model uses these input features:

- Open
- High
- Low
- Year
- Month

Target variable:

- Close

## Files

- `yes_bank_jupyter.ipynb`: Main notebook containing EDA, preprocessing, model building, and evaluation
- `data_YesBank_StockPrices.csv`: Dataset used for analysis
- `.gitignore`: Files and folders ignored by Git
- `README.md`: Project documentation

## Conclusion

The analysis showed that Open, High, Low, and Close prices are strongly related. Yes Bank stock showed major growth before 2018 and a sharp decline after that, indicating high volatility and risk. Linear Regression performed very well and was selected as the final prediction model.
