# Stock Price Prediction - NYSE
# Overview
The goal of this project is to develop a model that can predict stock prices for companies listed on the New York Stock Exchange (NYSE). We will use historical stock price data from 2016, split the data into training and testing sets, and utilize machine learning techniques to build and evaluate our predictive model.

# Data Description
The dataset includes the following files:

-prices.csv: Raw daily stock prices.
-prices-split-adjusted.csv: Daily stock prices adjusted for splits.
-securities.csv: General descriptions of each company, including sectors.
-fundamentals.csv: Metrics extracted from annual SEC 10K filings (2012-2016).
For this project, we primarily focus on prices.csv and securities.csv.

-prices.csv
Date: The date of the stock price.
Symbols: Ticker symbols for the companies.
Open: Opening price of the stock on the given date.
Close: Closing price of the stock on the given date.
Low: Lowest price of the stock on the given date.
High: Highest price of the stock on the given date.
-securities.csv
Ticker Symbol: Ticker symbol of the company.
Security: Name of the company.
GICS Sector: Type of company.
GICS Sub Industry: Sub-department of the company.
Address of headquarters: Headquarters location.
#Data Preparation
Loading the Data:

Read prices.csv and securities.csv.
Inspect and understand the structure and content of the data.
# Exploratory Data Analysis (EDA):

Display shape and column names.
Check for unique values, null values, and duplicate records.
Extract unique dates and ticker symbols.
# Data Selection:

-Select specific companies for detailed analysis: Yahoo Inc, Xerox Corp, Microsoft Corp, Facebook, Adobe Systems Inc, and Goldman Sachs Group.
Plot opening and closing stock prices for these companies over time.
# Data Processing
Feature Scaling:

-Use MinMaxScaler to scale stock prices between 0 and 1 for better model performance.
-Train-Test Split:

-Split the data into 80% training and 20% testing sets.
Data Preparation for Model:

-Create a function to prepare the data by using two previous values to predict the third value.
Reshape the data to 3D arrays to be used with LSTM (Long Short-Term Memory) and GRU (Gated Recurrent Unit) layers in our model.
Model Building
-Model Architecture:




# Results
The results demonstrate the model's performance in predicting stock prices. Key findings for selected companies are summarized below:

Adobe Systems Inc: Shows consistent growth in both open and close prices.
Facebook: Displays initial fluctuations followed by a significant upward trend.
Goldman Sachs Group: Experiences volatility but ends on a high note.
Microsoft Corp: Consistently rises, making it a favorable investment.
Xerox Corp: Struggles with progress, showing minimal growth.
Yahoo Inc: Steady prices initially, followed by effective progress.
Conclusion
The model successfully predicts stock prices using historical data. The combination of GRU and LSTM layers captures the temporal dependencies effectively. Further improvements can be made by incorporating additional features from fundamentals.csv and optimizing model parameters
