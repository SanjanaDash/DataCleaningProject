# DataCleaningProject
Data cleaning steps on NYC AirBnB dataset

FINAL PROJECT
README FILE – NYC AIRBNB
Group Members: Sanjana Dash, Sonam Kumari, Vishal Thadari

1. Use or create an original dataset (meaning that you haven't analyzed the dataset for this class before). Be sure to explain where your dataset comes from and where it can be found (or if you made it, how you made it). 

The datasets analyzed during the current project are available in the Kaggle and part of Airbnb dataset. These datasets were derived from the following public domain resources:
https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data
http://insideairbnb.com/new-york-city/

2. Identify what would make the dataset fit for use
As we know that most machine learning algorithms can’t work with poor data.
So, we tried to look for the following things: -

Check for human errors: -
As our data were done by humans so we checked some parts of the data and estimated that how often mistakes can happen

Is our data adequate for the task? 
The information which is provided. Is it sufficient for data analysis or do we need some more information? Once clean this can help us predict many aspects. It can be used to learn about different hosts and areas, which hosts are the busiest and why and is there any noticeable difference of traffic among different areas and what could be the reason for it.  

3. Evaluate if the data are fit for use or if cleaning will need to be done. If cleaning will need to be done, identify the cleaning steps that will be taken.
6. Document the cleaning steps that were taken (in a README, or OpenRefine log, or some other documentation mechanism).

Cleaning steps that we have taken: -
1.	Remove duplicate or irrelevant observations: Duplicate values happen when the same value or set of values appear in your data. It comes most often during data collection. when combining datasets from multiple places, scrape data or receive data from clients or multiple departments. 


Fix structural errors: When we are transferring data and notice some different looking strange naming conventions, typos, or incorrect capitalization. These inconsistencies can cause great trouble to the data. e.g.-> you may find some values like “999” or “abcd” in the data or incorrect date format in our case.

Filter unwanted outliers: Sometimes we see values that don't appear to fit in the data within the data that we are analyzing. Removing these outliers will help the performance of the data we are working with. We checked for ‘Minimum_nights’ and average came around 7 and then if checked for minimum_nights> 300, these were seen as outliers because staying in an Airbnb for more than 300days is not logically possible and might be a typo.

Handle Missing Data: Missing values are a very common type of error that we cannot ignore many algorithms will not accept missing values. There are a lot of ways to deal with missing values. 
In this project, we had few missing values and null values :
 
To deal with the above missing values, we checked if the number_of_reviews for that Airbnb was equals to zero, then last_review and reviews_per_month should also be zero.
We have dropped observations which had 'name' and ‘host_name’ as null, but by doing it we lost some information.

Validate and QA: At the end, we analyzed that our data is making some sense related to the work which we have to do and the outcome we need. We also performed standard scalling on the dataset for our future predictions.

7. Analyze the data. Were you able to answer your questions/meet your objectives with the cleaned dataset? If not, what else might need to be done?
In the end, we were able to analyze the prices, minimum nights, and availability.  We were able to learn about different hosts and areas, which hosts are the busiest and why and is there any noticeable difference of traffic among different areas and what could be the reason for it.  
In the future, we will try to dig deep into the data and will try to analyze and predict more information. We also feel we could manipulate some column values like no_of_reviews for a particular homestay are 0 then reviews_per_month should also be zero for it and hopefully once done, this can be used effectively for the purposes mentioned above.


4. Clean the dataset to make it fit for the project's use
5. Clean the dataset using at least one tool covered in this course (Excel, SQL, R, Python, etc.). (You don't have to use all of these!) But you need to use at least one.

We used Pandas as Pandas help efficiently handle large data, so we chose this method. We found this as an efficient method because it has less writing and more work is done. Pandas offer a diverse range of built-in functions that can be used to clean and manipulate datasets prior to analysis.
Presentation: https://prezi.com/p/fbr16usm9_yt/data-cleaning/



