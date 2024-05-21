# Forecasting the Stock Market with Artificial Intelligence (AI)

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
![change-volume](./Graphs%20&%20Images/pctchange-volume.png)

 The results of the linear regression analysis on $SPY’s percent change by volume reveal a statistical relationship between the trading volume and the daily percent change in stock prices.

![positive-month](./Graphs%20&%20Images/pctpositive-month.png)
![points-month](./Graphs%20&%20Images/points-month.png)

The histogram visualization of $SPY’s proportion of positive returns per month demonstrates the seasonal trends in stock market performance. By calculating the percentage of positive returns for each month and presenting it in a bar chart, the analysis provides a clear visual representation of when the market is more likely to experience gains.

![predicted-actual](./Graphs%20&%20Images/predicted-actual.png)

The predictive model demonstrates the capability of deep learning techniques in financial forecasting. By training the model on historical data and evaluating its performance using the mean squared error metric, the research provides a quantitative assessment of the model’s effectiveness. I was able to achieve 84% accuracy with the predictive model and 78% accuracy with the 'green/red' (second) model. The findings contribute to a better understanding of the stock market’s behavior and offer a foundation for further exploration in the field of financial analytics.

## Discussion

Correlation Between Volume and Stock Price: 
- My research on the correlation between trading volume and stock price is crucial because it provides insights into market liquidity and investor behavior. Other researchers have found that above-average and/or increasing trading volume can signal that traders are truly committed to a price move, and contrariwise, that below-average and/or decreasing volume can signal a lack of enthusiasm[[3]](https://www.schwab.com/learn/story/trading-volume-as-market-indicator#:~:text=An%20uptrend%20paired%20with%20increasing,buying%20and%20even%20higher%20prices). However, Schwab has also determined that inverse relationships between volume and price also exist, which aligns with my findings. This study found a correlation that suggests that volume can be a leading indicator of price movements, which is valuable for forecasting. This finding is consistent with existing literature that acknowledges volume as a determinant of price volatility and momentum. Altogether this information helps investors and market analysts in making informed decisions.

Effect of Time of Year on Market Behavior:
- The analysis of how time of the year affects markets is important as it can reveal temporal trends and calendar effects that influence market behavior. These insights are valuable for portfolio rebalancing and timing market entry or exit. It fits within the broader context of research that explores anomalies like the January effect or the end-of-quarter rebalancing; analysts at Trades That Swing found the same monthly fluxations[[4]](https://tradethatswing.com/seasonal-patterns-of-the-stock-market/). This study adds to this body of knowledge by providing a more granular view of how each month can impact market performance.

Interplay Between VIXM (Volatility) and Stock Price:
- Understanding the relationship between VIXM and stock prices is significant because it sheds light on how market volatility affects asset valuation. The VIXM, often referred to as the “fear index,” is an important measure of market risk. This study’s findings on this interplay can inform hedging strategies and risk assessment, guiding investors during periods of uncertainty and market turbulence.

Perspectives for Future Research:
- Going forward, one could examine the predictive power of seasonal trends with an emphasis on understanding time trends during different market cycles. Additionally, the interplay between VIXM and stock prices could be further investigated in the context of global economic events or policy changes. Future research with neural networks could also include the application of more robust machine learning techniques to enhance predictive models.

## Summary

This research project analyzes over two decades of stock market data, investigating patterns and correlations within major indices like SPY, QQQ, and DIA. Using advanced tools such as Pandas, NumPy, SciPy, Scikit-Learn, TensorFlow, and Keras, the study explores monthly trends, the relationship between trading volumes and returns, and the impact of volatility. Key findings include a statistical relationship between trading volume and daily percent change in stock prices, seasonal trends influencing market performance, and an 84% accurate predictive model, highlighting the effectiveness of deep learning techniques in financial forecasting. The discussion emphasizes the significance of these findings for informed decision-making, contributing valuable insights to financial analytics and offering actionable guidance for investors.

## References
[1] [Stock Data w/ Volume: Kaggle](https://www.kaggle.com/datasets/jacksoncrow/stock-market-dataset)

[2] [Download NASDAQ historical data](https://www.kaggle.com/code/jacksoncrow/download-nasdaq-historical-data/notebook)

[3] [Trading Volume as a Market Indicator](https://www.schwab.com/learn/story/trading-volume-as-market-indicator#:~:text=An%20uptrend%20paired%20with%20increasing,buying%20and%20even%20higher%20prices)

[4] [Best and Worst Months for the Stock Market – Seasonal Patterns](https://tradethatswing.com/seasonal-patterns-of-the-stock-market/)
