# StockPrices500

A small Streamlit app that lists the companies in the S&P 500 index and plots year-to-date closing prices for up to five of them.

This is an early learning project from January 2021. The code closely follows the S&P 500 app in Data Professor's "Build 12 Data Science Apps with Python and Streamlit" course on freeCodeCamp ([dataprofessor/streamlit_freecodecamp](https://github.com/dataprofessor/streamlit_freecodecamp)).

## What it does

- Scrapes the list of S&P 500 companies from [Wikipedia](https://en.wikipedia.org/wiki/List_of_S%26P_500_companies) with `pandas.read_html`.
- Lets you filter the table by GICS sector from a sidebar multiselect, and shows the filtered table with its row and column count.
- Offers the filtered table as a CSV download.
- Downloads year-to-date daily prices from Yahoo Finance with `yfinance` for the first 10 companies in the filtered list.
- A sidebar slider picks 1 to 5 companies, and the "Show Plots" button draws a closing price chart for each with matplotlib.

## Tech stack

Python, Streamlit, pandas, yfinance, matplotlib.

## Running it

There is no requirements file. Install the libraries the script imports (`closingPrice.py` also imports seaborn and NumPy, though it does not use them), plus `lxml` for `pandas.read_html`:

```bash
pip install streamlit pandas numpy matplotlib seaborn yfinance lxml
streamlit run closingPrice.py
```

The script was written against the Streamlit and yfinance releases of early 2021 and has not been updated since, so it may need small changes to run on current versions. It needs internet access to reach Wikipedia and Yahoo Finance.

## Author

Daniel Olliver, [danielolliver.com](https://danielolliver.com/)
