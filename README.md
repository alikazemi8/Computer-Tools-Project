# Computer-Tools-Project
CMSC6950 — Fall 2023

Trend Analysis code:

    This code offers an in-depth analysis of the S&P 500 index using its historical closing prices. 
    It employs a multifaceted approach to financial market analysis, encompassing several key areas:

    Trend Analysis: Utilizes simple and exponential moving averages (SMAs and EMAs) to identify market trends, 
    including identifying zones of bullish and bearish behavior and key crossover points like golden and death crosses.
    
    Statistical Measures: Conducts statistical analysis on moving averages, including calculating periods above and below 
    these averages and their respective percentage changes.
    
    Volatility Analysis: Examines the volatility of the market by calculating the Z-score of daily returns, 
    identifying extreme movements, and analyzing rolling volatility. 
    This section includes sensitivity analysis using various Z-score thresholds 
    to understand the frequency and intensity of market movements.
    
    Comparative Analysis: Extends the analysis to compare the S&P 500's behavior with other financial assets 
    like the US Dollar Index, Gold, Silver, and Bitcoin, focusing on their rolling volatilities.
    
    Technical Analysis: Applies technical analysis indicators such as the Moving Average Convergence Divergence (MACD) 
    and the Relative Strength Index (RSI).
    It generates buy and sell signals based on these indicators and calculates associated statistics, 
    such as average gains and losses.
    
    Duration Analysis: Calculates the duration and performance of bullish and bearish periods as indicated by RSI and MACD
    signals, providing insights into the effectiveness of these periods in terms of average gains and losses.
    
This comprehensive toolset provides a detailed perspective on the S&P 500's behavior, useful for traders, analysts, and anyone interested in understanding market dynamics. The code not only identifies key trends and movements in the stock market but also offers statistical insights and comparative analysis, making it a valuable resource for in-depth financial market analysis.



Prereqs:

    1- yfinance
    2- pandas
    3- matplotlib
    4- stats models
    5- numpy
    6- ta
    
    to install these you need to do:
    
    "pip3 install yfinance pandas matplotlib statsmodels numpy ta"
    
    in your terminal.
    
    
Code Steps:

        1. Data Retrieval:

            Step: The code retrieves historical data of the S&P 500 index from Yahoo Finance using yfinance.
            Output: A DataFrame sp500_data containing the historical data of the S&P 500 index.
            
        2. Simple Moving Average (SMA) Calculation:

            Step: Calculates 50-day and 200-day SMAs from the closing prices.
            Output: Two new columns in the DataFrame for 50-day SMA (sma50) and 200-day SMA (sma200).
            
        3. Exponential Moving Average (EMA) Calculation:

            Step: Calculates 50-day and 200-day EMAs from the closing prices.
            Output: Two additional columns for 50-day EMA (ema50) and 200-day EMA (ema200).
            
        4. Plotting Trends:

            Step: Plots the closing prices along with the calculated SMAs and EMAs.
            Output: Visual plots showing the S&P 500 closing prices with overlaid SMAs and EMAs.
            
        5. Seasonal Decomposition:

            Step: Decomposes the closing prices to analyze trend, seasonal, and residual components.
            Output: A plot showcasing the decomposed aspects of the S&P 500 data.
            
        6. Trend Identification:

            Step: Identifies bullish and bearish zones based on the position of the 50-day MA relative to the 200-day MA.
            Output: A plot with highlighted areas indicating bullish (green) and bearish (red) zones.
            
        7. Golden and Death Crosses Analysis:

            Step: Identifies golden and death crosses in the S&P 500 data.
            Output: Plots marking the points of golden and death crosses with additional statistics.
            
        8. Statistical Analysis:

            Step: Computes various statistics for periods above and below the 50-day and 200-day EMAs and SMAs.
            Output: Printed statistics such as maximum, average, and median days above/below the moving averages, 
            and percent  changes.
            
        9. Analysis of Crosses' Lagging Effect:

            Step: Analyzes the maximum percentage changes before golden and death crosses.
            Output: Printed information on the maximum percentage gains and losses before these crosses.
            
        10. Total Days Analysis:

            Step: Calculates the total number of days the S&P 500 stayed above or below the various moving averages.
            Output: Printed results showing the total days above/below each of the moving averages.
            
        11. Price Analysis:

            Step: Finds the lowest and highest closing prices and calculates the percentage gain.
            Output: Printed results showing the percentage gain from the lowest to the highest price in the dataset.
            
        12. Daily Gains and Losses Analysis:

            Step: Calculates average daily gains and losses under different market conditions.
            Output: Printed averages of daily positive gains and negative losses under specified conditions.
            
            
    
Customization:

    You can customize the following aspects if needed:
    
        1- Date Range: Modify the start and end parameters in the yf.download function to change the date range.
        2- Index/Ticker: Replace ^GSPC in the yf.download function with any other ticker to analyze a different stock or index.

Extended Analysis and Outputs:

        13. Z-Score Analysis of Daily Returns:

            Step: Calculates the Z-score for daily returns of the S&P 500 to identify how many standard deviations each return 
            is from the mean.
            Output: A new column in the DataFrame (Z-Score) showing the Z-score for each day's return.
            
        14. Identification of Extreme Movements:
    
            Step: Identifies extreme movements in the S&P 500, defined as days where the Z-score of the return is greater than 3.
            Output: A subset of sp500_data containing days with extreme movements.
            
        15. Rolling Volatility Calculation:

            Step: Calculates the 30-day rolling standard deviation (volatility) of the S&P 500's daily returns.
            Output: A new column (Rolling_Volatility) in the DataFrame representing the rolling volatility.
            
        16. Identification of High Volatility Periods:

            Step: Identifies periods of high volatility in the S&P 500, defined as times when the rolling volatility is greater
            than two times the mean rolling volatility.
            Output: A subset of sp500_data containing periods of high volatility.
            
        17. Plotting Extreme Values and Significant Events:

            Step: Creates a scatter plot highlighting extreme values (Z-score > 5) on top of the S&P 500 closing price line plot,
            with significant market events annotated.
            Output: A visual plot showing the S&P 500 closing prices, extreme values, and significant historical events like 
            the 2008 financial crisis and COVID-19 pandemic.
        
        18. Histogram of Daily Returns:

            Step: Generates a histogram of the S&P 500's daily returns using Seaborn.
            Output: A plot showing the distribution of daily returns for the S&P 500.
            
        19. Plot of Rolling Volatility Over Time:

            Step: Plots the 30-day rolling volatility of the S&P 500 over time.
            Output: A visual representation of how the S&P 500's volatility has changed over the selected time period.
            
        20. Comparative Analysis of Rolling Volatility:

            Step: Downloads historical data for the US Dollar Index (DXY), Gold ETF (GLD), Silver ETF (SLV), and Bitcoin 
            (BTC-USD) and calculates their 30-day rolling volatility.
            Output: Plots comparing the rolling volatilities of the S&P 500, USD, Gold, Silver, and Bitcoin.
            
        21. Analysis of Volatility Ranges:

            Step: Calculates the percentage of time each asset (S&P 500, USD, Gold, Silver, Bitcoin) spends in predefined 
            volatility ranges.
            Output: Printed results showing the distribution of each asset's volatility across different ranges.
            
 Sensitivity Analysis and Visualizations
 
        22. Calculation of Daily Returns:

            Step: Computes the daily percentage change in the S&P 500 closing prices.
            Output: A new column (Returns) in sp500_data showing the daily returns.
            
        23. Z-Score Calculation for Daily Returns:

            Step: Calculates the mean and standard deviation of daily returns, and then computes the Z-score for each return.
            Output: Updated sp500_data DataFrame with a new column (Z-Score) indicating the Z-score of daily returns.
            
        24. Identification of Extreme Movements:

            Step: Implements a function identify_extremes to identify extreme movements in the S&P 500 based on a specified 
            Z-score threshold.
            Output: A series of DataFrames for each Z-score threshold, each containing the days where the S&P 500's movements
            were considered extreme.
            
        25. Sensitivity Analysis Using Various Z-score Thresholds:

            Step: Conducts a sensitivity analysis using different Z-score thresholds (1, 2, 3, 4, 5) to understand the frequency
            of extreme movements in the S&P 500.
            Output: Printed counts of extreme values for each threshold, providing insight into how sensitive the S&P 500 is to
            different levels of deviation from the mean.
            
        26. Plotting Extreme Movements at Different Thresholds:

            Step: Creates a series of plots for each Z-score threshold, highlighting the extreme movements on the S&P 500 closing
            price chart.
            Output: Visual plots for each threshold, showing the S&P 500 closing prices with extreme values (based on the
            respective Z-score threshold) marked in red.
                       
 Technical Analysis and Trading Signal Generation
 
        27. Calculation of MACD (Moving Average Convergence Divergence):

            Step: Uses the ta library to calculate the MACD for the S&P 500 closing prices.
            Output: A new column (macd) in sp500_data representing the MACD values.
            
        28. MACD Buy/Sell Signal Generation:

            Step: Generates buy and sell signals based on the MACD values.
            Output: Two new columns in sp500_data, macd_buy and macd_sell, indicating the buy and sell signals respectively.
            
        29. Calculation of RSI (Relative Strength Index):

            Step: Calculates the 14-day RSI for the S&P 500 closing prices.
            Output: A new column (rsi) in sp500_data representing the RSI values.
            
        30. RSI Buy/Sell Signal Generation:

            Step: Generates buy and sell signals based on the RSI values.
            Output: Two new columns, rsi_buy and rsi_sell, indicating the buy and sell signals based on RSI.
            
        31. Plotting Technical Indicators:

            Step: Creates a multi-pane plot with the S&P 500 closing prices, RSI, and MACD indicators.
            Output: Visual plots showing the S&P 500 closing prices along with the RSI and MACD indicators, 
            including buy and sell signal points.
            
        32. Statistical Analysis of Buy/Sell Signals:

            Step: Implements a function calculate_statistics to compute statistics based on the buy/sell signals generated 
            by RSI and MACD.
            Output: Printed statistics for both RSI and MACD, including average, median, and maximum gains and losses, 
            providing insight into the effectiveness of these signals.
            
Duration Analysis of Bullish and Bearish Periods

        33. Calculating Duration and Performance of Trading Signals:

            Step: Implements a function calculate_total_signal_duration to calculate the total duration of bullish and bearish
            periods, as well as the average gains and losses during these periods, based on buy and sell signals 
            from RSI and MACD.
            Output: Total number of bullish and bearish days, and average bullish gains and bearish losses for both RSI and 
            MACD signals.
            
        34. Duration and Performance Analysis for RSI:

            Step: Applies the duration calculation function to the RSI buy and sell signals.
            Output: Printed statistics including the total number of bullish and bearish days, average bullish gain, 
            and average bearish loss based on RSI signals.
            
        35. Duration and Performance Analysis for MACD:

            Step: Applies the duration calculation function to the MACD buy and sell signals.
            Output: Printed statistics including the total number of bullish and bearish days, 
            average bullish gain, and average bearish loss based on MACD signals.