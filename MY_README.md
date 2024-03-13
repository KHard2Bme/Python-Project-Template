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

Client wants to create a coffee sales dashboard for years 2019 through 2022 so that they can have insight on the below requirements.

- Primary KPI: Total sales from all countries

             - Total transactions
  
             - Average sales
  
             - Minimum and Maximun sales.
              
- Secondary KPI:  Chart showing total sales in relation to countries

              - Sales total in relation to coffee type, roast type, coffee size
  
              . Chart showing total sales in each country
  
              - line chart showing trend of coffee type purchases over time
  
              - Bar chart showing top customers who purchased coffee. 



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


The original dataset has a column named Order Date which contains dates starting from 1/2/2019 through 8/18/2022.

There are missing dates in the Order Date column that total 638 days.

I used the MIN() and MAX() formulas to aid me in creating a date range series and then MATCH() to help pinpoint the missing dates.

The basic steps can be found in the "coffeeOrdersDataMissingdates.xlsx" file.


There are 12 months in each year except for year 2022 where we are missing September, October, November and December.



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
   - total sales $45,134, number of transactions 1,000, average sales $45.13, maximun sales $218.73 and minimum sales $2.69
   - by year
  
     
                2019- $12,187, 259, $47.05, $204.93, $2.69
 
                2020- $12,118, 263, $46.07, $189.75, $2.99
     
                2021- $13,766, 312, $44.12, $218.73, $2.69
     
                2022- $7,063, 166, $42.55, $204.93, $2.99
     - by country
    

               US -   $43,552, 960, $45.37, $218.73, $2.69  Most ordered coffee type is Excelsa-light(28% at $12,044),most ordered size is 2.5kg (53% at $22,901)
    
              Ireland -   $1,239, 28. $44.25, $178.71, $2.69   Most ordered coffee type is Liberica-Dark (36% at $800), most ordered size is 2.5kg (65% at $800)
       
              United Kingdom - $343,  12, $28.60, $83.84, $6.75  Most ordered coffee type is Excelsa-Dark (56% at $193), most ordered size is 0.5kg (32% at $11)

                
2.
 - US:  overall sales trend for Excelsa has been showing alot of up and down movement starting with $306 Q12019 to high $681 Q2,currently at lowest $41 Q12022

 - Ireland: overall sales trend for Liberica has been steady growth $88 Q12019 to high $179 Q42020, steady decline to lowest $23 Q42021,currently $43 Q12022

 - United Kingdom: overall sales trend for Excelsa has been steady growth $21 Q22019 through 2020, decline to lowest $12 Q42021,price skyrocketed $84 Q42021,currently at $22 Q12022
 
3. 
  Q22019 at $3,443 with there being 64 transactions and most ordered coffee type being Arabica (41%),most ordered coffee size 2.5kg (67% at $2,305) 
 
 
4. 
   February 2020 at $1,798 with there being 34 transactions and most ordered coffee type being Arabica (41%),most ordered coffee size 2.5kg (75% at $1352) 

5.
   United Kingdom
 
6.
  2021 Sept, total salses at $84 with 1 tranaction, loyalty card, coffee type Excelsa Dark and coffee size being 2.5 kg
   
7.
   2020 Oct, total sales at $12 with 1 transaction, loyalty card, coffee type Excelsa Medium and coffee size being 0.2kg
  
8. 
      7 customers have loyalty cards and total sales is $246

      2 customers paid a total of $20 for Excelsa Medium and Liberica Dark at 0.2kg

      2 customers paid a total of $82 for Arabica Dark and Liberica Medium at 0.5kg

      2 customers paid a total of $60 for Robusto Medium and Excelsa Light at 1kg

      1 customer paid a total of $84  for Excelsa Dark at 2.5kg

     
9. 
       Total sales in all regions for loyalty card holders is $20,918 with 479 transactions, coffee size 0.2kg ($1793), 0.5kg ($3062), 1kg ($4340) and 2.5kg ($11722)
   
       Total sales in all regions for those without a loyalty card is $24,216 with 521 transactions, coffee size 0.2kg ($1514), 0.5kg ($3968),1kg ($6670) and 2.5kg ($12,063)

       There is no advantage in being a loyalty card holder because you are paying the same price as regular customers.
   
   
       Unit Price: 0.2kg is on average $3.71

                   0.5kg is on average $7.44

                   1kg is on average $12.55

                   2.5kg is on average $28.45


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
