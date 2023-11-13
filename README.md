Fama-French Three-Factor Arbitrage Finder

Project Description

This project provides a Python script that automates the creation of a tracking portfolio based on the Fama-French three-factor model (Market Risk, Size, and Value) to uncover potential arbitrage opportunities. It dynamically fetches historical stock data, computes factor betas, and determines the optimal weights for a tracking portfolio.

Prerequisites
Before running the script, ensure you have the following:

- Python 3.x installed
- Required Python libraries: pandas, yfinance, statsmodels, sympy
- The Fama-French three-factor data file in CSV format, named Developed_3_Factors.csv, which is in teh repository as Developed_3_Factors 2.csv

Installation

To set up the necessary environment, run the following command to install the dependencies:

!pip install pandas yfinance statsmodels sympy

Usage

To use the script with custom stocks:

1. Modify the tickers list in the script to include the tickers of interest.
2. Set the stock_to_track variable to the ticker symbol of the stock you want to track.
3. Ensure the Fama-French factor data CSV is in the same directory as the script or update the file path in the script accordingly.

Customization

To analyze different stocks or timeframes:

- Update the tickers list with the new ticker symbols.
- Adjust the date range in the yf.download function call.

