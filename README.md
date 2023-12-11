# Predicting the Stock Market With Artificial Intelligence (AI)

## Abstract
This research project presents a comprehensive analysis of the stock market, utilizing a dataset that spans over two decades. The study focuses on identifying patterns and correlations between trading volumes, time of the year, volatility, and percent return correlations of major market indices such as SPY, QQQ, and DIA. The project is driven by a passion for financial markets and aims to uncover insights that could potentially inform investment strategies and market understanding.

## Introduction
The stock market is a complex and dynamic system influenced by various factors. This research delves into an extensive analysis of historical stock market data to explore monthly trends, the relationship between trading volumes and market returns, and the impact of volatility on market behavior. The study employs advanced analytical tools and methodologies to process and interpret the data, seeking to reveal significant patterns and anomalies.

## Overview
In this comprehensive project, I delve into a comprehensive stock market analysis, leveraging a dataset spanning 20+ years to extract valuable insights into the stock market.

As part of my analysis, I explore monthly trends to discern recurring patterns over the decades and investigate the relationship between volume, time of the year, volatility, and percent return correlations for the key market indices, SPY, QQQ, and DIA, aiming to uncover any evident patterns or trends.

In my analysis, I examine the correlation between trading volumes and daily returns of major market indices: S&P, Nasdaq, and Dow Jones Industrial Average (in the form of $SPY, $QQQ, $DIA), along with the influence of seasonal trends on market behavior. Additionally, I assess the impact of VIXM’s percentage change on these indices. By integrating these elements, I develop and validate a predictive model using SciKit-Learn that can forecast market returns.

This undertaking was inspired by my passion for the markets, and its primary objective is to unravel/reveal patterns, anomalies, and correlations within the extensive stock market data to address pivotal questions related to market behavior.

Throughout this project, I utilized various tools, including Python, Pandas, SciKit, and other relevant libraries, ensuring transparency and reproducibility in the analytical process. The following sections will expand upon the data selection, methodology, results, and discussions, providing a comprehensive view of the multifaceted analysis conducted on the stock market's historical data.

## Data Selection

The data processing and modeling were conducted using a Jupyter Notebook and are available [here](./Code/Stock-Data-Modeling_Notebook.ipynb).

The data used to analyze volume's correlation with stock price contained 20,000 with 7 features: Date, Open, High, Low, Close, Adjusted Close, and Volume.

The dataset can be found online on Google's data science competition platform, Kaggle [[1]](https://www.kaggle.com/datasets/jacksoncrow/stock-market-dataset), as well as the script used to collect the data [[2]](https://www.kaggle.com/code/jacksoncrow/download-nasdaq-historical-data/notebook).

Data preview:

![data screenshot](./Graphs%20&%20Images/stock-data.png)


## Methods
**Tools:**
- Data Analysis and Inference: NumPy, SciPy, Pandas, and Scikit
- Hosting/Version Control: GitHub
- IDE: Jupyter Notebook

**Inference methods:**

Graphing with Pandas & Matplotlib:
- Utilizing the Pandas library for its robust data manipulation capabilities, my work processes financial data from a CSV file to calculate and visualize the monthly returns of individual and (aggregated) sets of ETFs. The code employs Pandas’ read_csv function to load the data, to_datetime for date conversion, and groupby() combined with pct_change to compute the average monthly returns. These returns are then scaled to point values and plotted using Matplotlib, showcasing the power of Pandas in handling and analyzing time-series data for insightful financial trends.

Linear Regression with Scikit:
  - Opting for linear regression due to its simplicity and interpretability, my code calculates the daily percentage change in closing stock prices using the 'Close' column with the pct_change() method, converting decimals to percentages by multiplying by 100. To maintain a clean dataset, I utilized the dropna() method from Pandas to eliminate rows with NaN values resulting from the initial percentage change calculation, ensuring accuracy in further analysis or visualization.

Predictive Modelling with TensorFlow and Keras:
- Leveraging the advanced capabilities of TensorFlow and Keras for neural network architecture, alongside Scikit-Learn’s preprocessing tools, this approach involves constructing and evaluating a predictive model. The model is trained to predict the percent change in the S&P 500 Index ($SPY) by analyzing trading volume, the percent change in the Volatility Index (VIXM), and seasonal time factors. The effectiveness of the model is quantified using the mean squared error metric on a separate test dataset, demonstrating the integration of deep learning techniques for financial forecasting.


## Results
![change-volume](./Graphs%20&%20Images/pctchange-volume1.png)

 The results of the linear regression analysis on $SPY’s percent change by volume reveal a statistical relationship between the trading volume and the daily percent change in stock prices.

![positive-month](./Graphs%20&%20Images/pctpositive-month.png)
![points-month](./Graphs%20&%20Images/points-month.png)

The histogram visualization of $SPY’s proportion of positive returns per month demonstrates the seasonal trends in stock market performance. By calculating the percentage of positive returns for each month and presenting it in a bar chart, the analysis provides a clear visual representation of when the market is more likely to experience gains.

![predicted-actual](./Graphs%20&%20Images/predicted-actual.png)

The predictive model demonstrates the capability of deep learning techniques in financial forecasting. By training the model on historical data and evaluating its performance using the mean squared error metric, the research provides a quantitative assessment of the model’s effectiveness. I was able to achieve 84% accuracy with the predictive model and 78% accuracy with the 'green/red' (second) model. The findings contribute to a better understanding of the stock market’s behavior and offer a foundation for further exploration in the field of financial analytics.

## Discussion

What might the answer imply and why does it matter? How does it fit in with what other researchers have found? What are the perspectives for future research?	


## Summary
In this project I ...

## References
[1] [Stock Data w/ Volume: Kaggle](https://www.kaggle.com/datasets/jacksoncrow/stock-market-dataset)

[2] [Download NASDAQ historical data](https://www.kaggle.com/code/jacksoncrow/download-nasdaq-historical-data/notebook)
