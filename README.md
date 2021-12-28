# Web-Scraping-of-Stocks-websites
<h3>Web Scraping using Python</h3>
<br>
This is a project to scrape data from the web and store the results in both a text file as well as the SQLite
database.<br><br>
The CNN’s US Stock Market Movers website (https://money.cnn.com/data/hotstocks/) tracks the most active stocks on a
real time basis. First we collect the list of Most Actives tickers only from the above website.<br> <br>
Next, we take these ticker symbols and build a comma separated text file (called stocks.txt) with data about each stock from the Google finance
website: https://www.google.com/finance/quote/F:NYSE which gives the quote for ticker symbol
F as an example. The data collected from the Google Finance site includes (Actual text as seen in the website is in brackets):<br><br>
Previous close amount (PREVIOUS CLOSE)<br>
Avg. Volume (VOLUME)<br>
PE Ratio(TTM) (PE RATIO)<br>
<br>
Note that the stock average volume is an INTEGER type but the quantity obtained from the website
may have commas. The program removes these commas from the average volume quantity and stores it as numbers.<br><br>
In addition to the stocks.txt file, the data is also stored in an SQLite database called
StocksDatabase. The StocksDatabase has a table called StocksTable that contains the following columns and
types:<br><br>
Ticker Symb TEXT<br>
OpenPrice REAL<br>
Volume INTEGER<br>
PERatio REAL<br><br>
Every execution of the program creates a stocks.txt and StocksDatabase.db file in the
directory (deleting any existing files that were created) that the Python script is located and run.
