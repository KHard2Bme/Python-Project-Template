# Waze Review Sentiment Analysis 🚗 🚙
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
I will be performing an App Review Sentiment Analysis on the Waze mobile app dataset so as to evaluate and understand the sentiments expressed in user reviews over a 15 year span; 2009 through 2023.</b> 

I will use data analysis techniques to determine whether the sentiments in these reviews are positive, negative, or neutral.</b>

I will also perform Exploratory Data Analysis on the dataset to answer a few questions derived along the way.</b>


 >note: The App Review Sentiment Analysis and EDA steps will be shown in detail within the Jupyter Notebook.


# Python Libraries Used
---
*pandas, numpy, seaborn, matplotlip, datetime


# Data Sources
---

The primary dataset used for this analysis is the "WAZE_REVIEWS.csv" file obtained from Kaggle which contains real data.<br>

The dataset covers user reviews about the Waze app during years 2009 through 2023.<br>



# Exploratory Data Analysis
---
In my analysis I explore and answer the following questions:

1. From the distribution of ratings chart, which rating has the most reviews? Least reviews?
2. From the distribution of sentiments chart, What are the number of reviews for each sentiment?
3. Based off the findings from the sentiment distribution across ratings chart, the negative sentiment is at its highest in rating number 1. How many reviews make up this sentiment?
4. Based off the findings from the distribution of author apps versions chart, which version has the most reviews and which has the least?
5. Based off the findings from the sentiment distribution across apps chart, version 4.73.0.3 has more negative sentiments than version 3.9.4.0. How many negative reviews are in this sentiment? How many negative reviews are in 3.9.4.0?
6. Based off the findings from the distribution of years for reviews chart, which three years contained the most reviews and which year had the least amount of reviews overall?
7. Based off the findings from the sentiment distribution by year chart, the year with the most negative sentiments is 2021.How many negative reviews were placed and the percentage out of all negative sentiments?
8.  Based off the findings from the year distribution by ratings chart, We see that in rating number 1 there is a large percent of reviews from year 2021 than any other year. How many reviews make up the positive, negative and neutral sentiments?




# Summary of Findings
--- 
### Question 1: From the distribution of ratings chart, which rating has the most reviews? Least reviews?
![a](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/ba21b231-7bec-4b4b-a9bf-1b3abd3f5f3e)

- Rating number 5 has 523,774 reviews which makes up 67% of all the reviews.
- Rating number 2 has 23,109 reviews which makes up only 3% of all the reviews.



### Question 2:   From the distribution of sentiments chart, What are the number of reviews for each sentiment?
![B](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/5d8d0a7a-22b0-4816-8aa2-04a252957ea7)

- The positive sentiment has a total of 522,765 reviews which equates to 67% of all reviews.
- The neutral sentiment has a total of 207,918 reviews which equates to 27% of all reviews.
- The negative sentiment has a total of 44,861 reviews which equates to 6% of all reviews.



### Question 3: Based off the findings from the sentiment distribution across ratings chart, the negative sentiment is at its highest in rating number 1. How many reviews make up this sentiment?
![C](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/a007a824-a75d-48f3-84c1-2b962f5e807e)
![q3code](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/bd06fb86-c545-42c6-b625-18a46313e651)

There are a total of 21,987 reviews which make up the negative sentiment in rating number 1.

### Question 4: Based off the findings from the distribution of author apps versions chart, which version has the most reviews and which has the least?
![D](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/5734672d-590e-4049-b398-680937bfb881)


- version 3.9.4.0 has the most reviews being 28,448 which is 68% out of both versions.
- version 4.73.0.3 has the least reviews being 13,578 which is 32% out of both versions.




### Question 5:  Based off the findings from the sentiment distribution across apps chart, version 4.73.0.3 has more negative sentiments than version 3.9.4.0. How many negative reviews are in this sentiment? How many negative reviews are in 3.9.4.0?
![E](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/3e525613-f6da-43f0-9336-a31525fdd20a)

![q54254](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/c07be4de-3687-4a26-afe5-8b7734f4cad3)
![q51229](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/d11ac3de-be60-4c85-b9f6-7e16ed8de153)


- There are a total of 4,254 negative reviews within version 4.73.0.3 which is 78% out of both versions.
- There are a total of 1,229 negative reviews within version 3.9.4.0 which is 22% out of both versions.


### Question 6: Based off the findings from the distribution of years for reviews chart, which three years contained the most reviews and which year had the least amount of reviews overall?
![F](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/dfc7cfcd-5f21-4c34-8f28-2aebe1463101)

![q6years](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/c9e5cd3b-04a7-4b1f-b009-a6f17aab6602)

- Year 2016 has a total of 132,491 reviews which equates to 17% of all reviews in a 15 year span.
- Year 2017 has a total of 127,428 reviews which equates to 16% of all reviews in a 15 year span.
- Year 2015 has a total of 117,048 reviews which equates to 15% of all reviews in a 15 year span.
- Year 2009 has a total of 240 reviews which equates to 0.00030946 of all reviews in a 15 year span.



### Question 7: Based off the findings from the sentiment distribution by year chart, the year with the most negative sentiments is 2021.How many negative reviews were placed and the percentage out of all negative sentiments?
![G](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/ee17156b-97dc-4d8a-8c1e-2c0322cb8aff)

![q710383](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/38011c06-2510-4728-96cc-2df1f2f57985)

![q744861](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/aaeb1e50-b9be-41a8-bcae-76d409a2fbfb)


- For the year 2021, there was a total of 10,383 reviews placed which is 23% of all the negative sentiments.


### Question 8:  Based off the findings from the year distribution by ratings chart, We see that in rating number 1 there is a large percent of reviews from year 2021 than any other year. How many reviews make up the positive, negative and neutral sentiments?

![H](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/a29e9315-e1a2-435e-bdef-5049d0b6f5b1)


![q8pos](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/25420e12-fb44-4855-845a-96b97ec4e01a)

![q8neg](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/191194af-c154-4656-b11c-6992462cca1d)

![q8neu](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/11531f44-2ca1-429c-b102-dae0d88ebd13)

![q8total](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/8a7a53fb-453f-4f98-a4ce-a386f7e25844)

- For positive sentiments the total number is 2,047 which equates to 8% for 2021.
- For negative sentiments the total number is 9,413 which equates to 39% for 2021.
- For neutral sentiments the total number is 12,752 which equates to 53% for 2021.


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



