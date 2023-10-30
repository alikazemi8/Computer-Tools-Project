# Computer-Tools-Project
CMSC6950 — Fall 2023

Trend Analysis code:

    this code performs a trend analysis on the S&P500 index using it's historical closing prices.
    by leveraging simple and exponential moving averages, various trends, zones and notable cross points
    are indentified and usefull statistics are generated

Prereqs:

    1- yfinance
    2- pandas
    3- matplotlib
    4- stats models
    5- numpy
    
    to install these u need to:
    "pip3 install yfinance pandas matplotlib statsmodels numpy"
    in your terminal.
    
    
Code Steps:

        1- Data retrival: S&P500 data retrieved by the code from 1/1/2000 to 1/1/2023
    
    Trends:
    
        2- The code plots the raw data along with 50-day and 200-day SMA
            SMA: Simple Moving Average
        3- The code plots raw data along with 50-day and 200-day EMA
            WMA: Exponential Moving average
        4- Code plots a seasonal decompostions including 4 plots: the price chart, trend, seasonal and redisual components
    
    Trend identification:
    
        1- The code identifies bullish (where 50-day MA > 200-day MA) 
           and bearish (where 50-day MA < 200-day MA) zones and visualizes them.
        2- The code circles the Golden crosses and Death crosses on the price chart
            -> The "Golden Cross" is when the 50-day MA goes above the 200-day MA, 
                typically indicating a potential upward movement.
            -> The "Death Cross" is when the 50-day MA goes below the 200-day MA, 
                typically signaling a potential downward movement.
        
    Statistics Generations:
    
        1- Provides statistics for periods where the closing prices are above or below the specified SMAs and EMAs.
        2- Provides statistics specific to the periods between Golden and Death crosses.
        
Outputs:

    Graphs: The code will generate multiple plots showcasing:
        1- Closing prices with SMAs and EMAs.
        2- Bullish and bearish zones.
        3- Golden and Death crosses.
        4- Decomposition results.
    Statistics: Detailed statistics are printed for each of the conditions above.
    
Customization:

    You can customize the following aspects if needed:
    
        1- Date Range: Modify the start and end parameters in the yf.download function to change the date range.
        2- Index/Ticker: Replace ^GSPC in the yf.download function with any other ticker to analyze a different stock or index.