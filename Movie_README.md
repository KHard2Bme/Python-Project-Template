# A Quantitative Analysis of the Stock Market  💻
---

## Table of Contents

- [Project Overview](#project-overview)
- [Python Libraries Used](#python-libraries-used)
- [Data Sources](#data-sources)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Summary of Findings](#summary-of-findings)
- [Results from Findings](#results-from-findings)
- [Recommendations](#recommendations)

# Project Overview
---
We will be performing a <b>quantitative analysis</b> of five well known stocks and answer questions that can assist in the selection process of a wonderful stock; we will assume personal investment style is risk averse.

>note: Risk-averse investors prioritize the safety of principal over the possibility of a higher return on their money. They prefer liquid investments. 

The below selected stocks fall within the Consumer Cyclical sector, restaurants industry;
- <b>MCD</b>    McDonalds
- <b>SBUX</b>   Starbucks
- <b>CMG</b>    Chipotle Mexican Grill
- <b>YUM</b>    Yum! Brands
- <b>DRI</b>    Darden Restaurants



 To perform a quantitative analysis we will explore the below statistical concepts: 

  
 <p>
  
<b> 1.Descriptive Statistics:</b>     Summary statistics (mean, median, standard deviation, etc.) for each stock.<br>
  
<b> 2.Time Series Analysis:</b>         Trends and patterns over time, especially for closing prices.<br>

<b> 3.Volatility Analysis:</b>          How much the stock price fluctuates over a period.<br>

<b> 4.Correlation Analysis:</b>         How stock prices of different companies are related to each other.<br>

<b> 5.Comparative Analysis:</b>         Comparing the performance of different stocks.<br>

<b> 6.Risk-Return Trade-off Analysis:</b>  Analyzing the balance between the potential risks and rewards of different stocks,                                       aiding in portfolio management.<br>

 </p>
    
We will also compare the performance of the selected stocks against relevant benchmarks, such as market indices like the S&P 500.<br>  



>note: Statistical concepts will be shown in detail within Jupyter notebook.


# Python Libraries Used
---
*pandas, numpy, seaborn, matplotlip, datetime, yfinance*


# Data Sources
---

In order to make some good predictions I chose to collect one years worth of stock price data for McDonalds, Starbucks, Chipotle,Yum Brands and Darden restaurants.<br>

For this task, I used the Yahoo finance API (yfinance) to collect real-time stock market data from 03-13-2023 through 03-14-2024.<br>



# Exploratory Data Analysis
---
In my analysis I explore and answer the following questions:

1. What is the average closing price for each stock, standard deviation and how do these stocks compare?
2. What is the closing price for each stock as of 03-19-2024?
3. What is the minimum closing price for each stock? What trading day did this occur on?
4. Regarding the closing price for each stock, what are the trends and patterns over a one year timeframe and how do each compare? 
5. The volatility of the closing price gives us insight into how much the stock price fluctuates over a one year period. How does each stock rank in terms of volatility and in comparrison with each other?
6. The Correlation Analysis helps us understand how the stock prices of each company are related. What are the findings and what does this tell us?
7. With Comparative Analysis we can compare the performance of different stocks based on their returns over a one year period. What is the percentage change in closing prices of each stock and how do they compare with each other?
8. With the Risk-Return Trade-off Analysis stocks with higher average returns and lower risk are generally more desirable, but investment decisions often depend on the investor’s risk tolerance. What is the risk associated with each stock and how do they compare with each other?
9. Regarding the performance of each stock in comparisson to the S&P 500, what are their beta values and what does that number mean in comparison to the market movements?


# Summary of Findings
--- 
### Question 1: What is the average closing price for each stock, standard deviation and how do these stocks compare?
![describe](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/d400c6b3-5e11-47de-bd08-a1242b13c72e)


CMG (Chipotle Mexican Grill Inc.)
CMG shows the highest average closing price (<b>2097.45</b>) among these stocks and the highest standard deviation (<b>278.77</b>), indicating the most significant price fluctuation.

DRI (Darden Restaurants Inc.)
The average closing price is <b>157.77</b>, with a standard deviation of <b>9.16</b>.

MCD (McDonald's Corportation)
The average closing price is <b>284.25</b>, with a standard deviation of <b>12.45</b>, indicting more variability in closing prices compared to DRI, SBUX and YUM.

SBUX (Starbucks Corporation)
The average closing price is <b>98.35</b>, with a standard deviation of <b>5.22</b>, which has the smallest fluctuation in closing prices out of all the stocks.

YUM (Yum! Brands Inc.)
The average closing price is <b>131.09</b>, with a standard deviation of <b>5.61</b>.

Overall, SBUX and YUM show modest growth with slight fluctuation in closing prices, DRI shows a bit more variability followed by MCD, but it is CMG which has the most price fluctuation out of all the stocks.

### Question 2:  What is the closing price for each stock as of 03-19-2024? 
![3192024](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/21db24db-ce47-476c-8e3b-7ef59ca510cc)



MCD (McDonald's Corportation)
On 03-19-2024 the closing price is <b>283.15</b>.

SBUX (Starbucks Corporation)
On 03-19-2024 the closing price is <b>91.72</b>.

CMG (Chipotle Mexican Grill Inc.)
On 03-19-2024 the closing price is <b>2792.85</b>.

YUM (Yum! Brands Inc.)
On 03-19-2024 the closing price is <b>137.21</b>.

DRI (Darden Restaurants Inc.)
On 03-19-2024 the closing price is <b>173.65</b>.


### Question 3: What is the minimum closing price for each stock? What trading day did this occur on?

>note: The minimum closing price in comparrison to price on 03-19-2024 shows the price change and how it provided the perfect buying opportunity.

![mcd_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/d4d6aa6c-a2e3-485e-b89f-1a59dd59bb50)


MCD (McDonald's Corportation)
- The minumum closing price is <b>246.19</b> which took place on 10-12-2023
- In comparrison the closing price is <b>283.15</b> on 03-19-2024

![sbux_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/f9d2713f-59e4-4701-86b7-6e35b04413e4)


SBUX (Starbucks Corporation)
- The minumum closing price is <b>89.48</b> which took place on 10-03-2023
- In comparrison the closing price is <b>91.72</b> on 03-19-2024 

![cmg_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/9ed46c22-0090-4d01-b1ba-257589304e67)

CMG (Chipotle Mexican Grill Inc.)
- The minumum closing price is <b>1610.23</b> which took place on 03-20-2023
- In comparrison the closing price is <b>2792.85</b> on 03-19-2024 

![yum_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/bf948661-3ce1-47c1-8369-e3cc0fb7a72b)

YUM (Yum! Brands Inc.)
- The minumum closing price is <b>116.25</b> which took place on 10-12-2023
- In comparrison the closing price is <b>137.21</b> on 03-19-2024 

![dri_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/317e3f73-71fc-4a19-9703-a21fe071ea75)

DRI (Darden Restaurants Inc.)
- The minumum closing price is <b>134</b> which took place on 10-13-2023
- In comparrison the closing price is <b>173.65</b> on 03-19-2024 

### Question 4: Regarding the closing price for each stock, what are the trends and patterns over a one year timeframe and how do each compare? 
![NEW_timeseries](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/7220a477-19f6-4cc2-8d78-3b6b22e297b2)


The above plot displays the time series of the closing prices for each stock (MCD, SBUX, CMG, YUM, DRI) over a one year observed period. 
Let us next take a closer look at each stock individually so we can make an accurate reading.

![MCD_series](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/e2d145c4-b398-41cc-8cb5-844e0834db94)

![SBUX_series](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/863fe80e-a654-40f8-8f41-5f6f50b1f6d3)

![CMG_series](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/3da6923f-8be8-4b22-9d9e-0ed9072b2481)

![YUM_series](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/33a59301-589f-4901-8faa-a2423fd9c906)

![DRI_series](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/d1fd2466-16dd-4dd2-b044-892f95c858a0)




- Trend: Each stock shows its unique trend over time. For instance, AAPL and MSFT exhibit a general upward trend in this period.
- Volatility: There is noticeable volatility in the stock prices. For example, NFLX shows more pronounced fluctuations compared to others.
- Comparative Performance: When comparing the stocks, MSFT and NFLX generally trade at higher price levels than AAPL and GOOG in this dataset.


### Question 5: The volatility of the closing price gives us insight into how much the stock price fluctuates over a one year period. How does each stock rank in terms of volatility and in comparrison with each other?

![volatility_analysis](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/1cf03a18-aab0-49ff-b53e-1234f1c665e5)

NFLX: Highest volatility with a standard deviation of approximately 18.55.
MSFT: Next highest, with a standard deviation of around 17.68.
AAPL: Lower volatility compared to NFLX and MSFT, with a standard deviation of about 7.36.
GOOG: The least volatile in this set, with a standard deviation of approximately 6.28.
It indicates that NFLX and MSFT stocks were more prone to price fluctuations during this period compared to AAPL and GOOG.

### Question 6: The Correlation Analysis helps us understand how the stock prices of each company are related. What are the findings and what does this tell us?
![corr_analysis](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/95c86d97-1d8e-4cc7-8b8f-e1329dfafb00)

 Correlation Analysis to understand how the stock prices of these companies are related to each other:

From the heatmap, we can observe that there are varying degrees of positive correlations between the stock prices, with some pairs showing stronger correlations than others. For instance, AAPL and MSFT seem to have a relatively higher positive correlation.



### Question 7: With Comparative Analysis we can compare the performance of different stocks based on their returns over a one year period. What is the percentage change in closing prices of each stock and how do they compare with each other?
![compare_anaysis](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/14ef01ee-fea1-42a6-a16e-3d32125e83d4)

The bar chart and the accompanying data show the percentage change in the closing prices of the stocks from the start to the end of the observed period:

MSFT: The highest positive change of approximately 16.10%.
AAPL: Exhibited a positive change of approximately 12.23%. It indicates a solid performance, though slightly lower than MSFT’s.
GOOG: Showed a slight negative change of about -1.69%. It indicates a minor decline in its stock price over the observed period.
NFLX: Experienced the most significant negative change, at approximately -11.07%. It suggests a notable decrease in its stock price during the period.


### Question 8: With the Risk-Return Trade-off Analysis stocks with higher average returns and lower risk are generally more desirable, but investment decisions often depend on the investor’s risk tolerance. What is the risk associated with each stock and how do they compare with each other?
![daily_risk](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/71e3ee4c-bbf7-4083-aaef-d5e66f487852)

So, AAPL shows the lowest risk combined with a positive average daily return, suggesting a more stable investment with consistent returns. GOOG has higher volatility than AAPL and, on average, a slightly negative daily return, indicating a riskier and less rewarding investment during this period.

MSFT shows moderate risk with the highest average daily return, suggesting a potentially more rewarding investment, although with higher volatility compared to AAPL. NFLX exhibits the highest risk and a negative average daily return, indicating it was the most volatile and least rewarding investment among these stocks over the analyzed period.

### Question 9: Regarding the performance of each stock in comparisson to the S&P 500, what are their beta values and what does that number mean in comparison to the market movements?
![Beta](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/3195d4e6-c3b1-4293-8646-36a72ae45edc)



In the above code, we are assessing how sensitive Apple and Google stocks are to overall market movements, providing insights into their relative volatility and risk about the broader U.S. stock market represented by the S&P 500 index.

In the above output, the beta value for Apple is approximately 1.2257. This beta value suggests that Apple’s stock is estimated to be approximately 22.57% more volatile or sensitive to market movements (as represented by the S&P 500 index) compared to the overall market. The beta value for Google is approximately 1.5303. This beta value suggests that Google’s stock is estimated to be approximately 53.03% more volatile or sensitive to market movements.

A beta greater than 1 suggests that a stock tends to be more volatile than the market. In this case, both Apple and Google have beta values greater than 1, indicating that they are expected to be more volatile and sensitive to market movements. Google’s higher beta value (1.5303) compared to Apple’s (1.2257) suggests that Google’s stock is estimated to have a higher degree of market sensitivity or risk compared to Apple. Investors should consider this information when making investment decisions, as higher-beta stocks can provide greater potential for returns but also carry a higher level of risk.
   
# Results from Findings
---

# Recommendations
---









