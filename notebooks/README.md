# Stock Technical Analysis (Task 2)

This project performs quantitative analysis on historical stock price data for a predefined list of tickers. It focuses on calculating common technical indicators using the TA-Lib library and demonstrating basic financial metric calculation with PyNance, followed by data visualization.

This is part of a larger challenge focusing on financial news sentiment and stock market correlations.

## Data Source

The project uses locally available CSV files for historical stock data. Each CSV file should be named in the format `{TICKER}_historical_data.csv` (e.g., `AAPL_historical_data.csv`).

**Required CSV Columns:**
*   `Date` (parsable as datetime, will be set as index)
*   `Open`
*   `High`
*   `Low`
*   `Close`
*   `Volume`

## Setup & Prerequisites

This project is designed to be run in a **Google Colaboratory** environment.

**Libraries:**
*   `pandas`
*   `matplotlib`
*   `TA-Lib` (Requires special installation steps in Colab, which are included in the notebook: compiling from source.)
*   `pynance`
*   `yfinance` (Installed, though primary data is loaded locally for this task)

## How to Run

1.  **Open the Notebook:** Load the `.ipynb` file in Google Colab.
2.  **Upload Data:**
    *   In the Colab sidebar, navigate to "Files".
    *   Upload your stock data CSV files (e.g., `AAPL_historical_data.csv`, `TSLA_historical_data.csv`, etc.) to the root directory of the Colab session.
3.  **Verify Tickers:** Ensure the `tickers` list and corresponding filenames defined in Cell 3 of the notebook match your uploaded files.
4.  **Run Cells:** Execute the notebook cells sequentially.
    *   The first cell installs `TA-Lib` and other libraries. **You may need to restart the Colab runtime after this cell completes** for the libraries to be correctly loaded ("Runtime" > "Restart runtime").

## Key Analyses Performed

*   **Data Loading:** Loads historical stock data from local CSV files into a structured pandas DataFrame.
*   **Technical Indicators (using TA-Lib):**
    *   Simple Moving Averages (SMA - 20-day and 50-day)
    *   Relative Strength Index (RSI - 14-day)
    *   Moving Average Convergence Divergence (MACD)
*   **Financial Metrics (using PyNance):**
    *   Daily Returns (as a demonstration of PyNance capabilities)
*   **Visualization (using Matplotlib):**
    *   Plots of Close Price with SMAs.
    *   RSI plots, including overbought (70) and oversold (30) levels.
    *   MACD plots, including the MACD line, signal line, and histogram.