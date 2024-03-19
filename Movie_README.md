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
2. What is the closing price for each stock as of 03-14-2024?
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

![descriptive](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/b8dd14a7-55a4-433b-8bdc-2402cc8439ef)

CMG (Chipotle Mexican Grill Inc.)
CMG shows the highest average closing price (<b>2086.23</b>) among these stocks and the highest standard deviation (<b>276.39</b>), indicating the most significant price fluctuation.

DRI (Darden Restaurants Inc.)
The average closing price is <b>157.54</b>, with a standard deviation of <b>9.09</b>.

MCD (McDonald's Corportation)
The average closing price is <b>284.09</b>, with a standard deviation of <b>12.55</b>, indicting more variability in closing prices compared to DRI.

SBUX (Starbucks Corporation)
The average closing price is <b>98.42</b>, with a standard deviation of <b>5.17</b>.

YUM (Yum! Brands Inc.)
The average closing price is <b>131</b>, with a standard deviation of <b>5.59</b>.

Overall, SBUX, YUM and DRI all show modest growth with slight fluctuation in closing prices, MCD shows a bit more variability but it is CMG which has the most price fluctuation out of all the stocks.

### Question 2:  What is the closing price for each stock as of 03-14-2024? 
![3142024](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/adbd1cdf-3703-41fd-bee0-8a8e02c6cffa)



MCD (McDonald's Corportation)
On 03-14-2024 the closing price was <b>281.73</b>.

SBUX (Starbucks Corporation)
On 03-14-2024 the closing price was <b>91.66</b>.

CMG (Chipotle MExican Grill Inc.)
On 03-14-2024 the closing price was <b>2748.52</b>.

YUM (Yum! Brands Inc.)
On 03-14-2024 the closing price was <b>137.16</b>.

DRI (Darden Restaurants Inc.)
On 03-14-2024 the closing price was <b>171.77</b>.


### Question 3: What is the minimum closing price for each stock? What trading day did this occur on?

>note: The minumum closing price in comparrison to price on 03-14-2024 allows you to see what trading day provided the perfect buying opportunity.

![MCD_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/6560bcd2-a50f-4c56-9e91-561d1ecc2d3a)

MCD (McDonald's Corportation)
- The minumum closing price is <b>246.19</b> which took place on 10-12-2023
- In comparrison the closing price was <b>281.73</b> on 03-14-2024 

![SBUX_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/164eb712-7e9e-49c5-a23b-f57b76a77e94)

SBUX (Starbucks Corporation)
- The minumum closing price is <b>89.48</b> which took place on 10-03-2023
- In comparrison the closing price was <b>91.66</b> on 03-14-2024 

![CMG_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/268f10db-03c8-4c04-a8f8-f106e41f95f8)

CMG (Chipotle MExican Grill Inc.)
- The minumum closing price is <b>1590.87</b> which took place on 03-15-2023
- In comparrison the closing price was <b>2748.52</b> on 03-14-2024 

![YUM_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/33868a14-6632-4c66-9ef6-ba352ec30361)

YUM (Yum! Brands Inc.)
- The minumum closing price is <b>116.25</b> which took place on 10-12-2023
- In comparrison the closing price was <b>137.16</b> on 03-14-2024 

![DRI_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/0ab93139-d60f-4b0e-83dc-e2c607713e26)

DRI (Darden Restaurants Inc.)
- The minumum closing price is <b>134</b> which took place on 10-13-2023
- In comparrison the closing price was <b>171.77</b> on 03-14-2024 

### Question 4: Regarding the closing price for each stock, what are the trends and patterns over a one year timeframe and how do each compare? 

![time_series](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/e44f2a9d-5c81-4e33-84cb-1cd28d1f0cab)
The above plot displays the time series of the closing prices for each stock (MCD, SBUX, CMG, YUM, DRI) over a one year observed period. 

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
![corr_ananysis](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/b6acb344-c34a-402c-83b8-0d1a85ae4430)
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

![beta](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/c986655b-d555-4cfb-b327-a778587e5f6b)

In the above code, we are assessing how sensitive Apple and Google stocks are to overall market movements, providing insights into their relative volatility and risk about the broader U.S. stock market represented by the S&P 500 index.

In the above output, the beta value for Apple is approximately 1.2257. This beta value suggests that Apple’s stock is estimated to be approximately 22.57% more volatile or sensitive to market movements (as represented by the S&P 500 index) compared to the overall market. The beta value for Google is approximately 1.5303. This beta value suggests that Google’s stock is estimated to be approximately 53.03% more volatile or sensitive to market movements.

A beta greater than 1 suggests that a stock tends to be more volatile than the market. In this case, both Apple and Google have beta values greater than 1, indicating that they are expected to be more volatile and sensitive to market movements. Google’s higher beta value (1.5303) compared to Apple’s (1.2257) suggests that Google’s stock is estimated to have a higher degree of market sensitivity or risk compared to Apple. Investors should consider this information when making investment decisions, as higher-beta stocks can provide greater potential for returns but also carry a higher level of risk.
   
# Results from Findings
---

# Recommendations
---









# Coffee Sales Analysis                                                ☕

## Table of Contents

- [Project Overview](#project-overview)
- [Requirements](#requirements)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Pipeline](#data-pipeline)
- [Limitations](#limitations)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Summary of Findings](#summary-of-findings)
- [Results from Findings](#results-from-findings)
- [Recommendations](#recommendations)


![Final_D](https://github.com/KHard2Bme/Coffee_Sales_Dashboard_Excel/assets/146769989/b72ce4bf-cc41-4e5e-b7d2-d4fbcd0458d4)


### Project Overview
---

This data analysis project aims to provide insights into the sales performance of an e-commerce company over the past 4 years. By analyzing various aspects of the sales data, we seek to identify trends, make data-driven recommendations, and gain a deeper understanding of the company's performance.





### Requirements
---



### Data Sources
---

Sales Data: The primary dataset used for this analysis is the "coffeeOrdersData.xlsx" file, containing detailed information about each sale made by a ficticious company.






### Tools
---

- Excel - Data Cleaning, processing, analysis, report and dashboard creation.



      
## Data Pipeline
---

### 1. Data Cleaning

Data loading and inspection:
- Checking column header and rows for correct spelling, null values, extra spaces, datatypes and duplicates.

### 2. Data Processing
 
 Creation of customized columns utilizing the following formulas:
-  XLOOKUP(), IF(), IFERROR(),PROPER(), INDEX() & MATCH()


### 3. Data Analysis
 

Creation of Pivot tables, basic and customized charts

### 4. Report/Dashboard

Building of the dashboard as well as adding charts, timeline and slicers 
 

### Limitations
---




### Exploratory Data Analysis
---
Questions the client has that can now be answered;

1.What is the total sales, number of transactions, average sales, minimum and maximum sales for coffee in all regions from 2019 through 2022? by year? by country?

2. What is the overall sales trend for most ordered coffee type by country?
 
3. In the United States, what quarter had the most sales from 2019 to 2022?
 
4. In the United States, what month had the most sales from 2019 to 2022?

5. What country had the least amount of sales?
 
6. In the United Kingdom, what year and month had the highest sales; loyalty card holders, coffee type,roast type?
. 
7. In the United Kingdom, What month had the lowest sales; loyalty card holders, coffee type,roast type?

8.  How many customers in United Kingdom have Loyalty cards? Total sales? Purchased 0.2kg, 0.5kg, 1kg or 2.5kg size coffee?

9. Regarding total sales in all regions, is there any benefit in being a Loyalty Card holder vs. not?


## Summary of Findings
 
1.
   
### Results from Findings

The analysis results are summarized as follows:

1.  The United States makes up 96% of total sales within all regions, Ireland providing 3% followed by United Kingdom with a mere 1%
  
2.  With majority of sales coming from the United States the largest demand is for coffee type Excelsa, roast Light, and coffee size 2.5kg.

3.  Customers without loyalty cards have a slightly higher total sales and transaction count overall compared to those with a card. There is no special services applied to the loyalty card; for example, product discounts, accruel of points the more you spend, BOGO sales and possibly more delivery times ( overnight/next day ).
 
#### [Overall sales with no card is $24,216 with 521 transactions while those with a card is $20,918 with 479 transactions]



### Recommendations

Based on the analysis, we recommend the following actions:
- In order for the company to have more sales, special features and services need to be applied to the loyalty card.

- With a newly revamped loyalty card existing users would take advantage of the incentives and those without would be highly interested in applying for card; subscription and extra features fee can be applied.

- There needs to be more sales taking place within Ireland and the United Kingdom.

- A complete dataset would be beneficial in order to accertain the present health of the company and predict future trends; missing 683 days of information and the year 2022 missing 4 months of data.
