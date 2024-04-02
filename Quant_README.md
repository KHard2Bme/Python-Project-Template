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

The primary dataset used for this analysis is the "WAZE_REVIEWS.csv" file obtained from Kaggle which contains 780,073 rows and 9 columns.<br>

The dataset covers user reviews regarding the Waze app during the years 2009 through 2023.<br>

# Exploratory Data Analysis
---
<p>
In my analysis I explore and answer the following questions:

1. From the distribution of ratings chart, which rating has the most reviews? Least reviews?
2. From the distribution of sentiments chart, What are the number of reviews for each sentiment?
3. Based off the findings from the sentiment distribution across ratings chart, the negative sentiment is at its highest in rating number 1. How many reviews make up this sentiment?

### <h3 align="center">App Review Sentiments Analysis:<h3/>
-  I will perform a text analysis of the waze_data dataset to identify common words or themes within each sentiment category.
-  The analysis involves examining the most frequently occurring words in positive, negative, and neutral reviews using a word cloud.<br><br>


</p>


<p>  

 
4. Based off the findings from the distribution of author apps versions chart, which version has the most reviews and which has the least?
5. Based off the findings from the sentiment distribution across apps chart, version 4.73.0.3 has more negative sentiments than version 3.9.4.0. How many negative reviews are in this sentiment? How many negative reviews are in 3.9.4.0?

### <h3 align="center">App Review Sentiments Analysis:<h3/>
-  I will perform a text analysis on both author app versions 4.73.0.3 and 3.9.4.0 to identify common words or themes within the negative sentiment category.<br><br>



</p>

  
  
6. Based off the findings from the distribution of years for reviews chart, which three years contained the most reviews and which year had the least amount of reviews overall?
7. Based off the findings from the sentiment distribution by year chart, the year with the most negative sentiments is 2021.How many negative reviews were placed and the percentage out of all negative sentiments? How many negative reviews were from author app versions 4.73.0.3 and 3.9.4.0? 
8.  Based off the findings from the year distribution by ratings chart, We see that in rating number 1 there is a large percent of reviews from year 2021 than any other year. How many reviews make up the positive, negative and neutral sentiments? How many negative reviews were from author app versions 4.73.0.3 and 3.9.4.0?



# Summary of Findings
--- 
### Question 1: From the distribution of ratings chart, which rating has the most reviews? Least reviews?
![a](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/ba21b231-7bec-4b4b-a9bf-1b3abd3f5f3e)

- Rating number 5 has 523,774 reviews which makes up 67% of all the reviews.
- Rating number 2 has 23,109 reviews which makes up only 3% of all the reviews.


### [As you can see, the above distribution of ratings chart gives you a clear picture of how many reviews fall into each rating category (from 1 to 5)].

### Question 2:   From the distribution of sentiments chart, What are the number of reviews for each sentiment?
![B](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/5d8d0a7a-22b0-4816-8aa2-04a252957ea7)

### [In addition to the app having high ratings, reviewers also had many positive words in the reviews for the app.]

- The positive sentiment has a total of 522,765 reviews which equates to 67% of all reviews.
- The neutral sentiment has a total of 207,918 reviews which equates to 27% of all reviews.
- The negative sentiment has a total of 44,861 reviews which equates to 6% of all reviews.



### Question 3: Based off the findings from the sentiment distribution across ratings chart, the negative sentiment is at its highest in rating number 1. How many reviews make up this sentiment?
![C](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/a007a824-a75d-48f3-84c1-2b962f5e807e)

### [As you can see, most of the positive reviews fall within rating number 5 but most of the negative reviews fall within rating number 1].

![q3code](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/bd06fb86-c545-42c6-b625-18a46313e651)

There are a total of 21,987 reviews which make up the negative sentiment in rating number 1.

### <h3 align="center">App Review Sentiments Analysis:<h3/>
-  Let’s perform a text analysis of the waze_data dataset to identify common words or themes within each sentiment category.
![wc1p](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/0315c577-d2eb-41e5-9777-7122ab3f2551)
![wc1n](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/68705896-7828-4873-b540-747e1d559eb9)
![wc1ne](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/26bb99fd-7b44-4bec-ae00-c82ac3590c0d)

### [In addition to the app having high ratings and positive sentiments, reviewers also had many positive words in the reviews for the app.]

### Lets now take a look at two random author app versions to see how many reviews each has and how they compare with each other; 4.73.0.3 and 3.9.4.0.

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

### <h3 align="center">App Review Sentiments Analysis:<h3/>
-  Let’s perform a text analysis on both author app versions 4.73.0.3 and 3.9.4.0 to identify common words or themes in the negative sentiment to see if there are any major differences.<br><br>

<h3 align="center">(Author app version 4.73.0.3)<h3/>
 
![wc3neg](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/1ed4322c-53d9-4dcd-bae4-a72fd1807436)


<h3 align="center">(Author app version 3.9.4.0)<h3/>
 
![wc2neg3940](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/0504b6a8-b478-4e26-a3b7-ea638205a831)


### [As you can see, there are more negative words used in review text version 4.73.0.3 as opposed to version 3.9.4.0.]

### Lets now take a look at each of the years, how many reviews they each have and comparrisons.

### Question 6: Based off the findings from the distribution of years for reviews chart, which three years contained the most reviews and which year had the least amount of reviews overall?
![F](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/dfc7cfcd-5f21-4c34-8f28-2aebe1463101)

![q6years](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/c9e5cd3b-04a7-4b1f-b009-a6f17aab6602)

- Year 2016 has a total of 132,491 reviews which equates to 17% of all reviews in a 15 year span.
- Year 2017 has a total of 127,428 reviews which equates to 16% of all reviews in a 15 year span.
- Year 2015 has a total of 117,048 reviews which equates to 15% of all reviews in a 15 year span.
- Year 2009 has a total of 240 reviews which equates to 0.00030946 of all reviews in a 15 year span.



### Question 7: Based off the findings from the sentiment distribution by year chart, the year with the most negative sentiments is 2021.How many negative reviews were placed and the percentage out of all negative sentiments? How many negative reviews were from author app versions 4.73.0.3 and 3.9.4.0?
![G](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/ee17156b-97dc-4d8a-8c1e-2c0322cb8aff)

![q710383](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/38011c06-2510-4728-96cc-2df1f2f57985)

![q744861](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/aaeb1e50-b9be-41a8-bcae-76d409a2fbfb)
![4 73 0 3a](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/5882461d-0766-4d42-b938-1cddcd3a0c5a)
![3 9 4 0a](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/11a33773-a37d-4610-a063-71fc28973ff3)



- For the year 2021, there was a total of 10,383 reviews placed which is 23% of all the negative sentiments.
- Out of the 10,383 negative reviews 4,244(41%) of them are from the author app version 4.73.0.3, and 9(9%) are from version 3.9.4.0.


### Question 8:  Based off the findings from the year distribution by ratings chart, We see that in rating number 1 there is a large percent of reviews from year 2021 than any other year. How many reviews make up the positive, negative and neutral sentiments? How many negative reviews are from author app versions 4.73.0.3 and 3.9.4.0?

![H](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/a29e9315-e1a2-435e-bdef-5049d0b6f5b1)

![q8pos](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/4a5d34d1-720d-4ccf-b317-dd2513e54a95)
![q8neg](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/6539740b-c37d-4461-9db6-f994d715b6fb)
![q8neu](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/90253d38-f4dc-4388-8fc3-0a35026cee71)


![q8total](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/8a7a53fb-453f-4f98-a4ce-a386f7e25844)

![4 73 0 3b](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/66e2808b-a06b-45ac-a804-a7731b7656e0)

![3 9 4 0b](https://github.com/KHard2Bme/Python-Project-Template/assets/146769989/f191d2c9-8454-413b-93f8-5a50657d4d76)


- For positive sentiments the total number is 2,047 which equates to 8% for 2021.
- For negative sentiments the total number is 9,413 which equates to 39% for 2021.
- For neutral sentiments the total number is 12,752 which equates to 53% for 2021.
- Out of the 9,413 negative reviews in rating number 1 4,136(44%) of them are from the author app version 4.73.0.3, and 9(10%) are from version 3.9.4.0.


## Summary:

Based on the WAZE_REVIEWS.csv dataset we can tell that most of the user reviews have a very positive sentiment and are ranked within rating number 5.

Based on the two author apps reviewed 3.9.4.0 has twice the amount of reviews than 4.73.0.3, but version 4.73.0.3 has four times the amount of negative sentiment.

About 23% of the negative sentiments were placed in year 2021 with 41% coming from author app version 3.9.4.0 and 9% from version 4.73.0.3.

Of the negative sentiments placed in year 2021, those ranked in rating number 1 were 39%.

Of those ranked in rating number 1, 9% came from author app version 3.9.4.0, while 41% came from author app version 4.73.0.3.

Most of the reviews were made during 2014 through 2017.






