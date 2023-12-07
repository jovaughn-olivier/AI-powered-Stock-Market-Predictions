# Stock Market Predictions

## Overview

In this comprehensive project, I delve into a basic stock market analysis, leveraging a dataset spanning 20+ years to extract valuable insights into the stock market.

As part of my analysis, I explore monthly trends to discern recurring patterns over the decades and investigate the relationship between volatility, VOLQ (Nasdaq Volatility Index), and market downturns. My study also includes a detailed examination of daily volume and percent return correlations for the key market indices, SPY, QQQ, and DIA, aiming to uncover any detectable? patterns or trends. Additionally, a daily average return function is employed to provide a nuanced understanding of daily market dynamics.

This undertaking was inspired by my passion for the markets, and its primary objective is to unravel/reveal patterns, anomalies, and correlations within the extensive stock market data to address pivotal questions related to market behavior.

Throughout this project, I utilized various tools, including Python, Pandas, and other relevant libraries, ensuring transparency and reproducibility in the analytical process. The following sections will expand upon the data selection, methodology, results, and discussions, providing a comprehensive view of the multifaceted analysis conducted on the stock market's historical data.

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
