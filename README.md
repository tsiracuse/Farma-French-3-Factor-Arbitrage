

To run this code, copy and paste it into google colab or any jupyter notebook and make sure that the Developed_3_Factors 2.csv is in the repository

The notebook fama-french-3-factor-arbitrage-algorithm.ipynb encapsulates a robust method for arbitrage detection utilizing the Fama-French three-factor model. It orchestrates the entire process from data procurement and preprocessing to computation and analysis. Initially, it sources the Fama-French factor data, incorporating market risk, size, and value premiums alongside the risk-free rate. Subsequent data cleaning ensures accuracy, especially concerning any missing values denoted by -99.99.

A regression analysis for each selected stock against these factors yields beta coefficients, encapsulating each stock's sensitivity to market variables. Leveraging these betas, the script formulates factor equations and computes the expected returns for the stocks under consideration.

The core of this algorithm lies in the strategic assembly of an arbitrage portfolio. Through a systems of equations solver, it meticulously calculates the precise weights of the selected stocks and the risk-free asset, aiming to match a target stock's factor exposures. The concluding step involves the computation of the portfolio's alpha to identify potential arbitrage opportunities, thus providing a theoretical yet insightful lens into market inefficiencies

Relevant Equations 

<img width="718" alt="Screen Shot 2023-11-13 at 6 54 33 PM" src="https://github.com/tsiracuse/Farma-French-3-Factor-Arbitrage/assets/80054149/0d7d0269-6c9c-465a-9040-dc280cf2533a">

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
Here is an example where X_stock1 is the weight corresponding the first emelemtn in the tickers list excluding the target stock 
<img width="1215" alt="Screen Shot 2023-11-13 at 6 57 41 PM" src="https://github.com/tsiracuse/Farma-French-3-Factor-Arbitrage/assets/80054149/d7c7e711-8565-4dd5-a793-a4ffbe9ca32a">
