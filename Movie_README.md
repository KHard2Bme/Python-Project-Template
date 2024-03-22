# A Quantitative Analysis of the Stock Market  💻
---

## Table of Contents

- [Project Overview](#project-overview)
- [Python Libraries Used](#python-libraries-used)
- [Data Sources](#data-sources)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Summary of Findings](#summary-of-findings)
- [Results from Findings](#results-from-findings)


# Project Overview
---
We will be performing a <b>quantitative analysis</b> of five well known stocks and answer questions that can assist in the selection process of a wonderful stock; we will assume personal investment style is risk averse.

>note: Risk-averse investors prioritize the safety of principal over the possibility of a higher return on their money. 

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

For this task, I used the Yahoo finance API (yfinance) to collect real-time stock market data from 03-20-2023 through 03-19-2024.<br>



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

MCD (McDonald's Corportation):
- Q1 through Q22023 shows the stock price moving in an upward trend, then mid Q2 the price follows a sporadic sideways movement until begining of Q32023 where there is a trend reversal and the closing price follows a downward trend to the lowest price being <b>$246.19</b> on <b>10-12-2023</b>. There is a sudden trend reversal which continues upward into Q12024 and levels off into another sporadic sideways movement.

![SBUX_series](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/863fe80e-a654-40f8-8f41-5f6f50b1f6d3)

SBUX (Starbucks Corporation):
- Q1 through Q22023 shows the stock price gradually moving in an upward fluctuating trend until mid Q2 where there is a major trend reversal and the price follows a bearish market run with significant sideways movement until the lowest price is reached, that being <b>$89.48</b> on <b>10-03-2023</b>. There is a sudden trend reversal which continues slightly upward into Q42023, it continues until end of Q4 and the trend changes once more fluctuating downward into a sideways movement within Q12024.

![CMG_series](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/3da6923f-8be8-4b22-9d9e-0ed9072b2481)

CMG (Chipotle Mexican Grill Inc.):
- Q12023 starts out at the lowest closing price of the year being <b>$1610.23</b> on <b>3-20-2023</b>. The stock gradually follows an upward trend until Q22023 and soon experiences significant sideways movement until mid Q32023. The trend reverses and there is a sporadic down trend until Q42023, a sudden trend reversal follows with a gradual upward trend into Q12024.

![YUM_series](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/33a59301-589f-4901-8faa-a2423fd9c906)

YUM (Yum! Brands Inc.):
- Q1 through Q22023 shows the stock price gradually moving in an upward trend until mid Q2, there is a sudden trend reversal where price fluctuates in a downward trend to the lowest closing price being <b>$116.25</b> on <b>10-12-2023</b>. There is a another sudden trend reversal which shows continued fluctuation upward into Q12024.

![DRI_series](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/d1fd2466-16dd-4dd2-b044-892f95c858a0)

DRI (Darden Restaurants Inc.):
- Q1 through Q22023 shows the stock price following a downward sideways movement until end of Q2, were there is a trend reversal and the price fluctuates upward until mid Q32023. There is a trend reversal and the closing price follows a volatile downward trend until hitting lowest price, that being <b>$134</b> on <b>10-13-2023</b>. There is another trend reversal which takes place and the price steadily climbs upward into Q12024. 

 ### Comparrison:

 <b>Trend:</b> 
 - MCD, YUM and DRI all experience their lowest closing prices in Q42023 (10-12-2023 for MCD and YUM, 10-13-2023 for DRI).
 - Each stock experienced a trend reversal in Q42023 which followed a sporadic upward trend into Q12024 except SBUX, this stock had another trend reversal end of Q42023       and closing prices fluctuated downward into a sideways movement within Q12024.

 <b>Volatility:</b>
- There is noticeable volatility in each of the stock prices. For example, CMG shows more pronounced fluctuations compared to all the others.

 <b>Comparative Performance:</b>
- When comparing the stocks, DRI, YUM and SBUX generally trade at price levels close in range as opposed to MCD which is a bit higher in price. CMG trades at a substancially higher price than all the other stocks in this dataset.


### Question 5: The volatility of the closing price gives us insight into how much the stock price fluctuates over a one year period. How does each stock rank in terms of volatility and in comparrison with each other?

![volatility_analysis](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/1cf03a18-aab0-49ff-b53e-1234f1c665e5)

CMG: Highest volatility with a standard deviation of approximately 275.90.<br> 
MCD: Next highest, with a standard deviation of around 12.47.<br>
DRI: Volatility rating right after MCD, with a standard deviation of around 9.12.<br>
YUM: Slight volatility compared to others, with a standard deviation of about 5.61.<br>
SBUX: The least volatile in this set, with a standard deviation of approximately 5.21.<br>

In summary, CMG stock is more prone to price fluctuations during this period than compared to MCD, DRI, YUM and SBUX.
YUM and SBUX closing prices are relatively steady, while DRI and MCD shows a bit more price changes.

### Question 6: The Correlation Analysis helps us understand how the stock prices of each company are related. What are the findings and what does this tell us?
![corr_analysis](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/95c86d97-1d8e-4cc7-8b8f-e1329dfafb00)

 From the heatmap, we can observe that there are varying degrees of positive and negative correlations between the stock prices, with some pairs showing stronger correlations than others.
- MCD and YUM have a relatively higher positive correlation than any other stocks (0.82).
- This makes perfect sense since both have very similar closing price trends and patterns over the past year 


### Question 7: With Comparative Analysis we can compare the performance of different stocks based on their returns over a one year period. What is the percentage change in closing prices of each stock and how do they compare with each other?
![compare_anaysis](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/14ef01ee-fea1-42a6-a16e-3d32125e83d4)


CMG: The highest positive change of approximately 79.05%.<br>
DRI: Exhibited a positive change of approximately 8.07%.It indicates a solid performance.<br>      
MCD: Exhibited a positive change of approximately 5.85%.It also indicates a solid performance, though slightly lower than DRI and YUM.<br>
SBUX: Experienced the most significant negative change, at approximately -7.53%. It suggests a notable decrease in its stock price during a one year period.<br>
YUM: Exhibited a positive change of approximately 7.00%. It indicates a solid performance, slightly lower than DRI but higher than MCD.<br>


### Question 8: With the Risk-Return Trade-off Analysis stocks with higher average returns and lower risk are generally more desirable, but investment decisions often depend on the investor’s risk tolerance. What is the risk associated with each stock and how do they compare with each other?
![daily_risk](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/71e3ee4c-bbf7-4083-aaef-d5e66f487852)

- MCD: shows the lowest risk combined with a positive average daily return, suggesting a more stable investment with consistent returns.
- YUM: has a slightly higher volatility and daily returns than MCD, showing slightly more of a reward in investment.
- DRI: shows moderate risk with the second highest average daily return, suggesting a potentially more rewarding investment, although with higher volatility compared to MCD and YUM.
- SBUX: exhibits the second highest risk and has a negative average daily return, indicating a riskier and less rewarding investment during this period.
- CMG: exhibits the highest risk but has the highest average daily return, indicating it was the most volatile but provided the most rewarding investment among these stocks over the analyzed period.

### Question 9: Regarding the performance of each stock in comparisson to the S&P 500, what are their beta values and what does that number mean in comparison to the market movements?

>note: A beta greater than 1 suggests that a stock tends to be more volatile than the market.<br>

![beta](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/0b681c7c-2d6c-412c-8d90-3776d272f152)

In the above code, we are assessing how sensitive McDonalds, Starbucks, Chipotle, Yum and Darden stocks are to overall market movements, providing insights into their relative volatility and risk about the broader U.S. stock market represented by the S&P 500 index.


The beta value for McDonalds is approximately -0.02210,-2.21% more volatile or sensitive to market movements.<br>
The beta value for Starbucks is approximately 0.06466, 6.47% more volatile or sensitive to market movements.<br>
The beta value for Chipotle is approximatley 0.01268, 1.27% more volatile or sensitive to market movements.<br>
The beta value for Yum is approximatly -0.02636, -2.64% more volatile or sensitive to maket movements.<br>
The beta value for Darden is 0.07123, 7.12% more volatile or sensitive to market movements.<br>

## Summary:
- Starbucks, Chipotle and Darden all have beta values less than 1, indicating that they are expected to be less volatile and sensitive to market movements.
- McDonalds and Yum both have negative values which suggest they move in opposite direction to overall market movements. Although rare, there are some stocks in the market that have a negative beta<br>

# Results from Findings
---
As a reminder, I will be making a determination of a wonderful stock to pick from the viewpoint of an investor who is risk averse.

 After performing a Quatitative Analysis of five well known stocks in the restaurant industry; (MCD) McDonalds, 
(SBUX) Starbucks, (CMG) Chipotle Mexican Grill, (YUM) Yum! Brands and (DRI) Darden Restaurants, within a one year time period of 3-20-2023 through 3-19-2024, the data shows that <b>(DRI) Darden Restaurants</b> would be the best choice.


  Factors which helped in the decision process were outcomes from the below statistical concepts:
 
 - <b>Comparative Analysis:</b>    Out of all five stocks we looked at SBUX experienced the most significant negative change, at approximately -7.53%.
  This left us with four stocks to analyze.

 - <b>Risk-Return Trade-off Analysis:</b>  CMG exhibited the highest risk out of all the stocks though having the highest average daily return.
  We would have to remove this stock from the lineup, leaving us with three.

 - <b>Performance against the S&P500:</b>  MCD and Yum both have negative values which suggest they move in opposite direction to overall market movements.
    For some, both stocks might be good because they act as a hedge against market downturns and can help reduce portfollio risks. For the average investor looking to make daily returns this might be a market risk. 
    This leaves us with DRI as the wonderful stock to purchase; beta value is 0.07123 which is far below a beta of 1.









