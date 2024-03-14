# A Quantitative Analysis of the Stock Market
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





# Python Libraries Used
---
*pandas, numpy, seaborn, matplotlip, datetime, yfinance*


# Data Sources
---

In order to make some fairly good predictions I chose to collect one years worth of stock price data for McDonalds, Starbucks, Chipotle,Yum Brands and Darden restaurants.<br>

For this task, I used the Yahoo finance API (yfinance) to collect real-time stock market data from 03-13-2023 through 03-13-2024.<br>



# Exploratory Data Analysis
---
In my analysis I explore and answer the following questions:

1. What are the most profitable movies and how much should you spend?
2. Which movie genres are most commonly produced and does quantity equate to higher net profits?
3. What is the best time of the year to release a movie?
4. Which actors and directors tend to add the most value?
5. How much money should you spend to win an Oscar?
6. What impact, if any, does runtime and movie rating have on Net Profit, Profit Margin and IMDb rating?
7. Sticking to our analysis of Net Profit and Profit Margin, what should our Company determine to be the baseline for sustainable success?
8. Based on the success of current competitors, which should we look to for best practices?

# Summary of Findings
--- 
1.
   
# Results from Findings
---

# Recommendations
---




## Question 1: What are the most profitable movies and how much should you spend?

To answer this question and provide a recommendation we'll make use of a budgets dataframe called `imdb_budgets_df`. Our analysis will require that we use the data to calculate profit and profit margin.

```
imdb_budgets_df['Profit'] = imdb_budgets_df['Worldwide Gross'] - imdb_budgets_df['Production Budget']

imdb_budgets_df['Profit_Margin'] = (imdb_budgets_df['Worldwide Gross'] - 
                                    imdb_budgets_df['Production Budget'])/imdb_budgets_df['Worldwide Gross']
```

We will also create two columns called `Adjusted_Budget` and `Adjusted_Profit` where we recalculate a movie's budget and profit to account for inflation and allow us to perform analysis based on the value of the 2020 dollar.

We examine the overall trend of budget versus profit to see if there's any correlation.

![BudgetVProfit](visuals/BudgetVProfit.png)

We also take a look at the top 25 movies in terms of profit to understand their financial success and how closely we should attempt to emulate their budget. We can see in the graph below there are a few outliers so the median will end up being more useful in determining our final budget.

![ProfitBudgetTop25](visuals/ProfitBudgetTop25.png)

**Question 1 Conclusion:** Our Company should budget \$82,250,000 for a movie and that budget should correlate with a profit margin of 80\%.

## Question 2: Which movie genres are most commonly produced and does quantity equate to higher net profits?

We first count the number of movies in each genre and plot those results on a bar graph.
```
m_by_genre = genre_budgets_df.groupby('Genre', as_index=False)['Movie'].count().sort_values(by='Movie', ascending=False)
```
Using the same `groupby` method, we select the median net profit and profit margin for each genre. We use the median in this case as the mean is likely skewed by outliers. Outliers could either be movies with enormous profits or movies having negative profit.

![NetProfitGenre.png](visuals/NetProfitGenre.png)

![ProfitMarginGenre](visuals/ProfitMarginGenre.png)

Lastly, we look at the percent of net profit by genre. This informs us as to how Our Company should allocate their movie budget to various films.

**Question 2 Conclusion:** Animation, adventure, and sci-Fi have the highest net profit of all genres. Analysis of profit margin shows that in addition animation, adventure, and sci-fi, horrors and musicals also have financial success.

## Question 3: What is the best time of the year to release a movie?

We start by converting the dates from the `imdb_budgets_df` dataframe to a datetime object.  We then do a count by month to see the number of movies released in each month.

When grouping by month, we can select the `Net Profit` and `Profit Margin` columns so that we can see which months have the most financial success.

![MarginByMonth](visuals/MarginByMonth.png)

Finally we plot the net profit by month for a small selection of genres.  We can see that there is a general trend amongst these genres for the profit in each month.

![ProfitbyMonthbyGenre](visuals/ProfitbyMonthbyGenre.png)

**Question 3 Conclusion:** We recommend that Our Company release the bulk of their movies, especially Animation, during the summer months (i.e. May-July). Adventure, Drama and Comedy movies would see similar success if released in November, but the recommendation remains to focus on summer.

## Question 4: Which actors and directors tend to add the most value?

In this section we are going to take a look at the average net profit across all movies. From there we want to determine which actors and directors consistently appear in movies where the net profit substantially exceeds the average. We will represent this in a field called Value Above Replacement(VAR). To further simplify this concept; if across all movies the average net profit is 100 dollars and the average net profit of movies from 'Actor: X' is 200 dollars he/she would have a VAR of 2. This number represents X times over the average. To eliminate outliers we will look at actors who appear in 10 or more movies and directors who work in 5 or more.

We'll use the `actors_df` dataframe, adjust for inflation, and calculate profit as we did in Question 1. Then filter by actors who have starred in 10 or more movies.

```
actor_counts = actors_df['value'].value_counts()
actor_list = actor_counts[actor_counts >= 10].index.tolist()
actors_df = actors_df[actors_df['value'].isin(actor_list)]
```

To calculate VAR:
```
actor_total = actors_df.groupby(['value'],  as_index=False)['Net Profit'].mean().sort_values(by='Net Profit', ascending=False)
actor_total['VAR'] = (actor_total['Net Profit']/actor_total['Net Profit'].mean())
```
We follow the same process with directors, except we filter by using 5 or more movies instead of 10.

![VARActor](visuals/VARActor.png)

![VARDirector](visuals/VARDirector.png)


**Question 4 Conclusion:** We recommend that Our Company focus their cast and crew search to individuals who consistently score at least 1.0 on the VAR score. We can, with a high level of confidence, conclude that these individuals will elevate the overall production.

## Question 5: How much money should you spend on a movie to win an Oscar?

In this analysis we will join the `imdb_budgets_df` and `awards_df` dataframes so that we explore correlations between budgets and Oscar wins. We first look at a distribution of the budget for movies that have been Oscar-nominated.  We also look at the win rates for the nominated movies so that we can establish the minimum number of nominations required to secure at least one win. For this analysis the minimum number or nominations 
required was three.

![Oscar_Nominated](visuals/Oscar_Nominated.png)

We use three nominations as the cutoff to filter our data and then look at the distribution of budgets again. We use the median as our measure of central tendency due to a large standard deviation in the data.

![3_Nominations](visuals/3_Nominations.png)

**Question 5 Conclusion:** Our Company should spend at least $35,465,000 in order to make an Oscar-winning movie.

## Question 6: What impact, if any, does runtime and movie rating have on Net Profit, Profit Margin and IMDb rating?

To answer this question we will only focus on the 4 ratings: G, PG, PG-13, and R. We then count the ratings to see how many movies fall within each category.  From there we can examine the net profit and profit margin of genre to see which has the most financial success.

It's also important to see the net profits of each rating by genre. We first do a `groupby` on rating and genre and then create a pivot table so that we can see the net profits of each rating in each genre.  This will guide us as to what ratings should be targeted based on the genre of the movie being made.

![ProfitbyGenrebyRating](visuals/ProfitbyGenrebyRating.png)

**Question 6 Conclusion:** We recommend that Microsoft take into consideration the rating of the movie based on the genre and target audience. If making animation movies, it is wise to stick to a G or PG rating, otherwise PG-13 is the sweetspot. In terms of runtime, there is little correlation in terms of overall profitability.

## Question 7: Sticking to our analysis of Net Profit and Profit Margin, what should Microsoft determine to be the baseline for sustainable success?

This analysis will require the use of the `studiobudgets_df dataframe`.  We first drop non-pertinent rows so that we can just focus on the studio performance. As we've done with other analyses, we use `groupby` and select the median as the primary measure of central tendency.
We only select the top 25 studios as we are concerned with both being financial successful as well as being recognized as one of the major studios in the industry.


![NetProfitStudio](visuals/NetProfitStudio.png)

**Question 7 Conclusion:** Our Company should aim for a profit margin of 66% and a net profit of slightly over 50 million per movie to compete with the top existing studios.

## Question 8: Based on the success of current competitors, which should we look to for best practices?

We take the `theaters_df` dataframe and a column called `dollars_per_theater` to see what the average domestic gross per theater is for a movie.  We then `groupby` by studio so that we can compare each studio.

![DomesticPerTheater](visuals/DomesticPerTheater.png)


We also investigate the correlation between the average maximum number of theaters and average domestic gross per studio.

![TheatersVGross](visuals/TheatersVGross.png)

We perform a join between the `theaters_df` and `awards_df` dataframes to further explore this question.
```
theaters_df.set_index(['title', 'year'], inplace=True)
theaters_and_awards = theaters_df.join(awards_df, how='inner', on=['title', 'year'])
```

The joining only leaves us with 66 movies upon which to draw conclusions.  That is not ideal, but two studios - Disney and Warner Bros. - stand out among the rest as they have 22 and 15 of the movies in this dataframe, respectively. This is more than double any other studio.  We then compare 
their average domestic gross per theater and win rate to see which of the two has performed better.


**Question 8 Conclusion:** Our Company should look towards Disney based upon domestic gross per theater and win rate. This means that Our Company should on average target for a movie to be in a maxium of 3818 theaters at its peak. 


### Dataset Source and Overview

The FIFA 21 dataset used in this project was obtained from a data cleaning challenge on Twitter which I was a part of.
It consists of player attributes, statistics and other relevant information.

The original FIFA21 dataset contains 18K+ records of player data. Each record represents a unique player and includes
various attributes such as player name, age, nationality, club, overall rating and more.

### Issues found in the data

During the initial exploration and analysis of the FIFA21 dataset, several issues were identified including:

- Missing values - The Hits and Loan Date End columns had missing values which required careful handling and computation.
- Inconsistent formatting - This was observed across different columns making it necessary to standardize the data
  for consistency. The Heights and Weights columns each had values stored in different units.

### Tools Used

For the data cleaning project, the following tools and libraries were used:

1. **Python** for data cleaning tasks.
2. **Pandas** was instrumental in data manipulation, cleaning and handling missing values.
3. **NumPy** was utilized for mathematical operations and array handling during the cleaning process.
4. **Jupyter Notebooks** provided an interactive environment for code development, exploration and documentation.

### Data Cleaning Process

The data cleaning process involved the following steps:
1. **Data Understanding** - The dataset was thoroughly examined to understand the structure, columns and their meanings.
   The data did not have a data dictionary attached. With the help of online sources I was able to create one that helped me
   gain an understanding of what all the columns represented.
2. **Data Exploration** - Exploratory Data Analysis was performed to gain insights into the data, identify patterns and uncover anomalies.
3. **Handling missing values** - Through the EDA performed, I quickly realised there was a valid reason for the missing values in the Hits and Loan Date End columns.
   The Hits column represented the number of times a player had been searched in the FIFA database. Since some players had never been searched, their records were blank.
   For the Loan Date End column, this represented when the contracts for players who were *On Loan* would end. Since some of the players were free and others
   on contract, their records were left blank.
4. **Standardizing formatting** - Inconsistent formatting issues eg the values in the Heights and Weights columns that were stored with different units were resolved by
   applying transformations, lambda functions and data normalization techniques.
5. **Validation and quality checks** - The cleaned dataset underwent rigorous validation to ensure the quality, accuracy and integrity of the data.

### Documentation

For detailed information about the data cleaning process, please refer to the Jupyter notebooks provided in the repository as well as the YouTube link provided above.
They contain step by step explanations, code samples and documentation showing each stage of the data cleaning process.
A template to help facilitate the same if you would like to follow along from the YouTube video is also provided within this repository.


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
