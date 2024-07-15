# prophet-challenge
for this assignment I had to analyze data from multiple DataFrames for MercadoLibre. 

I uploaded my notebook to google collab and imported my dependencies as a first step.
I used import matplotlib.pyplot as plt to be able to genrerate plots and figures

- In the first step of the assignment I was tasked with finding unusual patterns in the search traffic.

The code for storing the data in a pandas DataFrame was already given to me 

* I sliced the DataFrame to show the search traffic for the month of May of 2020 and plotted the data for that month 
* Afterwards I calculated the sum of the search traffic for May 2020 and the monthly median search traffic for all months in order to find the search traffic ratio of May in comparison to the rest of the year
* These calculations showed that there was a very slight increase in the search traffic when the company released its financial results. Although the increase is barely noticable as the ratio was 1.08

- In step 2 I was tasked mine the data for predictable seasonal patterns in order to maximize benefits of the company's efforts such as marketing.

* I grouped the the hourly search data using the groupby function and plotted the data to showcase what time of the day had the most search traffic
* I did the same thing again but to visiualize the data for days of the week
* I then did that to visiualize the data for week of the year

- In the third step I needed to find if there is a connection between the search data and stock price 

* The stock price DataFrame was already given and uploaded in the starter file
* I plotted the stock prices
* I concatenated the stock prices DataFrame with the search trends DataFrame
* I sliced the DataFrames so the only show data from January to June of 2020
* I plotted the columns close and search trends separately using the syntax plot(subplots=True) which was given to me in the instructions
* I created an additional column called Lagged Search Trends to shift the search traffic by one hour
* I created a column called Stock Volatility to calculate the standard deviation of the closing stock price return data and then plotted the stock volatility column
* I also created a column that calculates the hourly return percentage of the closing price called Hourly Stock Return
* I created a table that to show if there is a correlation between StocK Volatility, Search Trends, and Hourly Stock Return

- In step 4 I needed to created a time series model with Prophet

* I relabeled the columns Date and search trends so that the syntax is recognized by Prophet and dropped the null values from the DataFrame
* I called the Prophet function and fit the time series model 
* I created a future dataframe to hold predictions for 2000 hours ahead
* I plotted the Prophet predictions for the trends data
* I plotted the individual time series components to be able to find answers for when the search traffic is greates and lowest during the time of day, week, and year.