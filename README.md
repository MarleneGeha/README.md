# README.md
import yfinance as yf

# Extracting Tesla stock data
tesla_data = yf.download('TSLA', start='2023-01-01', end='2024-01-01')

# Reset the index
tesla_data.reset_index(inplace=True)

# Display the first five rows
print(tesla_data.head())


 import requests
from bs4 import BeautifulSoup
import pandas as pd

# Send a GET request to the Tesla revenue page
url = "https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue"
response = requests.get(url)

# Parse the HTML content
soup = BeautifulSoup(response.text, "html.parser")

# Find the revenue table
table = soup.find_all('table')[1]  # Assuming revenue table is the second table on the page

# Convert the HTML table to a pandas DataFrame
tesla_revenue = pd.read_html(str(table))[0]

# Display the last five rows
print(tesla_revenue.tail())
import yfinance as yf

# Extracting GameStop stock data
gme_data = yf.download('GME', start='2023-01-01', end='2024-01-01')

# Reset the index
gme_data.reset_index(inplace=True)

# Display the first five rows
print(gme_data.head())


import yfinance as yf

# Extracting GameStop stock data
gme_data = yf.download('GME', start='2023-01-01', end='2024-01-01')

# Reset the index
gme_data.reset_index(inplace=True)

# Display the first five rows
print(gme_data.head())
import requests
from bs4 import BeautifulSoup
import pandas as pd

# Send a GET request to the GameStop revenue page
url = "https://www.macrotrends.net/stocks/charts/GME/gamestop/revenue"
response = requests.get(url)

# Parse the HTML content
soup = BeautifulSoup(response.text, "html.parser")

# Find the revenue table
table = soup.find_all('table')[1]  # Assuming revenue table is the second table on the page

# Convert the HTML table to a pandas DataFrame
gme_revenue = pd.read_html(str(table))[0]

# Display the last five rows
print(gme_revenue.tail())

import matplotlib.pyplot as plt

def make_graph(dataframe, title):
    plt.figure(figsize=(10, 6))
    plt.plot(dataframe['Date'], dataframe['Close'], label='Close Price')
    plt.xlabel('Date')
    plt.ylabel('Price ($)')
    plt.title(title)
    plt.legend()
    plt.grid(True)
    plt.show()

# Assuming tesla_data contains the Tesla stock data dataframe
make_graph(tesla_data, title="Tesla Stock Price")

import matplotlib.pyplot as plt

def make_graph(dataframe, title):
    plt.figure(figsize=(10, 6))
    plt.plot(dataframe['Date'], dataframe['Close'], label='Close Price')
    plt.xlabel('Date')
    plt.ylabel('Price ($)')
    plt.title(title)
    plt.legend()
    plt.grid(True)
    plt.show()

# Assuming gme_data contains the GameStop stock data dataframe
make_graph(gme_data, title="GameStop Stock Price")




















