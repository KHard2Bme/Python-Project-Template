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
We will be performing a <b>quantitative analysis</b> of five well known stocks and answer a few questions that will assist someone in the selection process of a wonderful stock; based upon personal investment strategy.

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

For this task, I used the Yahoo finance API (yfinance) to collect real-time stock market data from 03-13-2023 through 03-13-2024.<br>



# Exploratory Data Analysis
---
In my analysis I explore and answer the following questions:

1. What is the closing price for each stock as of 03-14-2024?
2. WHat is the average closing price for each stock, standard deviation and how do these numbers help in comparring each?
3. What is the minimum closing price for each stock? What trading day did this occur on?
4. Regrding the closing price for each stock, what are the trends and patterns over a one year timeframe and how do each compare? 
5. The volatility of the closing price gives us insight into how much the stock price fluctuates over a one year period. How does each stock rank in terms of volatility and in comparrison with each other?
6. The Correlation Analysis helps us understand how the stock prices of each company are related. What are the findings and what does this tell us?
7. With Comparative Analysis we can compare the performance of different stocks based on their returns over a one year period. What is the percentage change in closing prices of each stock and how do they compare with each other?
8. With the Risk-Return Trade-off Analysis stocks with higher average returns and lower risk are generally more desirable, but investment decisions often depend on the investor’s risk tolerance. What is the risk associated with each stock and how do they compare with each other?
9. Regarding the performance of each stock in comparisson to the S&P 500, what are their beta values and what does that number mean in comparison to the market movements?


# Summary of Findings
--- 
### Question 1:  What is the closing price for each stock as of 03-14-2024? 
![3142024](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/99795063-5dbc-4fb2-be9a-d272f510a8f0)




MCD (McDonald's Corportation)
On 03-14-2024 the closing price was <b>281.94</b>.

SBUX (Starbucks Corporation)
On 03-14-2024 the closing price was <b>91.66</b>.

CMG (Chipotle MExican Grill Inc.)
On 03-14-2024 the closing price was <b>2748</b>.

YUM (Yum! Brands Inc.)
On 03-14-2024 the closing price was <b>137.20</b>.

DRI (Darden Restaurants Inc.)
On 03-14-2024 the closing price was <b>171.87</b>.


### Question 2: What is the average closing price for each stock, standard deviation and how do these numbers help in comparring each?

![descriptive](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/d8445ada-a744-4b4f-8bde-a3de30482ee1)


MCD (McDonald's Corportation)
The average closing price is <b>284.03</b>, with a standard deviation of <b>12.59</b>.

SBUX (Starbucks Corporation)
The average closing price is <b>98.46</b>, with a standard deviation of <b>5.15</b>, indicating less variability in closing prices compared to MCD.

CMG (Chipotle MExican Grill Inc.)
CMG shows the highest average closing price (<b>2081.62</b>) among these stocks and the highest standard deviation (<b>274.88</b>), indicating the most significant price fluctuation.

YUM (Yum! Brands Inc.)
The average closing price is <b>130.96</b>, with a standard deviation of <b>5.58</b>.

DRI (Darden Restaurants Inc.)
The average closing price is <b>157.45</b>, with a standard deviation of <b>9.06</b>.


### Question 3: What is the minimum closing price for each stock? What trading day did this occur on?

>note: The minumum closing price in comparrison to price on 03-14-2024 allows you to see what trading day provided the perfect buying opportunity.

![MCD_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/0b059ffb-c356-42ed-b685-1485ba5b55ca)
MCD (McDonald's Corportation)
- The minumum closing price is <b>246.19</b> which took place on 10-12-2023
- The closing price was <b>281.94</b> On 03-14-2024 

![SBUX_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/be4fe367-1104-42cf-9b13-c7f02d8a751a)
SBUX (Starbucks Corporation)
- The minumum closing price is 89.48	 which took place on 10-03-2023

![CMG_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/bf8562b6-ddb4-44e6-8a1a-f963b8610bdb)

CMG (Chipotle MExican Grill Inc.)
- The minumum closing price is 1590.76 which took place on 03-14-2023

![Yum_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/6f405f97-8f6e-487d-8a10-cb57785a01b1)

YUM (Yum! Brands Inc.)
- The minumum closing price is 116.25 which took place on 10-12-2023

![DRI_min](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/ef5e6ae7-1880-4dd5-b210-6b74f42658ab)

DRI (Darden Restaurants Inc.)
- The minumum closing price is 134 which took place on 10-13-2023


### Question 4: Regrding the closing price for each stock, what are the trends and patterns over a one year timeframe and how do each compare? 


### Question 5: The volatility of the closing price gives us insight into how much the stock price fluctuates over a one year period. How does each stock rank in terms of volatility and in comparrison with each other?


### Question 6: The Correlation Analysis helps us understand how the stock prices of each company are related. What are the findings and what does this tell us?


### Question 7: With Comparative Analysis we can compare the performance of different stocks based on their returns over a one year period. What is the percentage change in closing prices of each stock and how do they compare with each other?


### Question 8: With the Risk-Return Trade-off Analysis stocks with higher average returns and lower risk are generally more desirable, but investment decisions often depend on the investor’s risk tolerance. What is the risk associated with each stock and how do they compare with each other?


### Question 9: Regarding the performance of each stock in comparisson to the S&P 500, what are their beta values and what does that number mean in comparison to the market movements?




   
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
