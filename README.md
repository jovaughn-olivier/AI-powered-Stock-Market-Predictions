# Stock Market Predictions

## Overview

In this comprehensive project, I delve into a comprehensive stock market analysis, leveraging a dataset spanning 20+ years to extract valuable insights into the stock market.

As part of my analysis, I explore monthly trends to discern recurring patterns over the decades and investigate the relationship between volume, time of the year, volatility, and percent return correlations for the key market indices, SPY, QQQ, and DIA, aiming to uncover any evident patterns or trends.

In my analysis, I examine the correlation between trading volumes and daily returns of major market indices: S&P, Nasdaq, and Dow Jones Industrial Average (in the form of $SPY, $QQQ, $DIA), along with the influence of seasonal trends on market behavior. Additionally, I assess the impact of VIXM’s percentage change on these indices. By integrating these elements, I develop and validate a predictive model using SciKit-Learn that can forecast market returns.

This undertaking was inspired by my passion for the markets, and its primary objective is to unravel/reveal patterns, anomalies, and correlations within the extensive stock market data to address pivotal questions related to market behavior.

Throughout this project, I utilized various tools, including Python, Pandas, SciKit, and other relevant libraries, ensuring transparency and reproducibility in the analytical process. The following sections will expand upon the data selection, methodology, results, and discussions, providing a comprehensive view of the multifaceted analysis conducted on the stock market's historical data.

## Data Selection

The data processing and modeling were conducted using a Jupyter Notebook and are available [here](./Code/Stock-Data-Modeling_Notebook.ipynb).

The data used to analyze volume's correlation with stock price contained 5300–6800 samples with 7 features: Date, Open, High, Low, Close, Adjusted Close, and Volume.

The dataset can be found online on Google's data science competition platform, Kaggle [[1]](https://www.kaggle.com/datasets/jacksoncrow/stock-market-dataset), as well as the script used to collect the data [[2]](https://www.kaggle.com/code/jacksoncrow/download-nasdaq-historical-data/notebook).

Data preview:

![data screenshot](./Graphs%20&%20Images/stock-data.png)


## Methods
Tools:
- Data Analysis and Inference: NumPy, SciPy, Pandas, and Scikit
- Hosting/Version Control: GitHub
- IDE: Jupyter Notebook


Inference methods used with Scikit:
- Linear Regression Model
  - Opting for linear regression due to its simplicity and interpretability, my code calculates the daily percentage change in closing stock prices using the 'Close' column with the pct_change() method, converting decimals to percentages by multiplying by 100. To maintain a clean dataset, I utilized the dropna() method from Pandas to eliminate rows with NaN values resulting from the initial percentage change calculation, ensuring accuracy in further analysis or visualization.
 



- The averaging of the percent changes is done using the groupby function in pandas, which is a powerful tool for aggregating data. Here’s a step-by-step explanation:-
- Concatenate the dataframes: All the individual dataframes for each ticker are concatenated into one large dataframe. This is done using pd.concat(dfs). The resulting dataframe has an entry for each date for each ticker.
- Group by date: The groupby('Date') function is used to group the data by date. This means that for each date, all the entries (i.e., percent changes for each ticker) are grouped together.
- Calculate the mean: The mean() function is then applied to each group. This calculates the average percent change for each date across all tickers. The result is a new dataframe where the index is the date and the ‘PercentChange’ column contains the average percent change for that date.
- So, if you have three tickers (SPY, DIA, QQQ) and for a particular date, the percent changes are 0.5%, -0.3%, and 0.2%, the average percent change for that date would be (0.5 - 0.3 + 0.2) / 3 = 0.13%.
- This method gives you the average return of the portfolio consisting of the given tickers, assuming equal weight for each ticker. If the weights are not equal, you would need to calculate a weighted average instead.
 

## Results


## Discussion
...
xyz
....

## Summary
In this project I ...

## References
[1] [Stock Data w/ Volume : Kaggle](https://www.kaggle.com/datasets/jacksoncrow/stock-market-dataset)

[2] [Download NASDAQ historical data](https://www.kaggle.com/code/jacksoncrow/download-nasdaq-historical-data/notebook)
