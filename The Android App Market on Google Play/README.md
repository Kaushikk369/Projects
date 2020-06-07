
# The Android App Market on Google Play
## Project Description  
Mobile apps are everywhere. They are easy to create and can be lucrative. Because of these two factors, more and more apps are being developed. In this project, you will do a comprehensive analysis of the Android app market by comparing over ten thousand apps in Google Play across different categories. You'll look for insights in the data to devise strategies to drive growth and retention.  


This project lets you apply the skills from Data Manipulation with pandas. We recommend that you have taken this course before starting this project.


The [data](https://www.kaggle.com/lava18/google-play-store-apps) for this project was scraped from the [Google Play](https://play.google.com/store/apps?hl=en) website. While there are many popular datasets for Apple App Store, there aren't many for Google Play apps, which is partially due to the increased difficulty in scraping the latter as compared to the former. The data files are as follows:
- **`apps.csv` : contains all the details of the applications on Google Play. There are 13 features that describe a given app.**   
- **`user_reviews.csv` :  contains 100 reviews for each app, [most helpful first](https://www.androidpolice.com/2019/01/21/google-play-stores-redesigned-ratings-and-reviews-section-lets-you-easily-filter-by-star-rating/). The text in each review has been pre-processed and attributed with three new features: Sentiment (Positive, Negative or Neutral), Sentiment Polarity and Sentiment Subjectivity.**   
## Project Task
 - Google Play Store apps and reviews   
 - Data cleaning
 - Exploring app categories
 - Distribution of app ratings
 - Size and price of an app
 - Relation between app category and app price
 - Filter out "junk" apps
 - Popularity of paid apps vs free apps
 - Sentiment analysis of user reviews   

## 1. Google Play Store apps and reviews
Mobile apps are everywhere. They are easy to create and can be lucrative. Because of these two factors, more and more apps are being developed. In this notebook, we will do a comprehensive analysis of the Android app market by comparing over ten thousand apps in Google Play across different categories. We'll look for insights in the data to devise strategies to drive growth and retention. 

 ![Alt Text](google_play_store.png)   
## 2. Data cleaning
The four features that we will be working with most frequently henceforth are Installs, Size, Rating and Price. The info() function (from the previous task) told us that Installs and Price columns are of type object and not int64 or float64 as we would expect. This is because the column contains some characters more than just [0,9] digits. Ideally, we would want these columns to be numeric as their name suggests.   
   
Hence, we now proceed to data cleaning and prepare our data to be consumed in our analyis later. Specifically, the presence of special characters (, $ +) in the Installs and Price columns make their conversion to a numerical data type difficult.   

## 3. Exploring app categories
With more than 1 billion active users in 190 countries around the world, Google Play continues to be an important distribution platform to build a global audience. For businesses to get their apps in front of users, it's important to make them more quickly and easily discoverable on Google Play. To improve the overall search experience, Google has introduced the concept of grouping apps into categories.   
This brings us to the following questions:
- Which category has the highest share of (active) apps in the market?   
- Is any specific category dominating the market?   
- Which categories have the fewest number of apps?   
   
We will see that there are 33 unique app categories present in our dataset. Family and Game apps have the highest market prevalence. Interestingly, Tools, Business and Medical apps are also at the top.   
## 4. Distribution of app ratings   
After having witnessed the market share for each category of apps, let's see how all these apps perform on an average. App ratings (on a scale of 1 to 5) impact the discoverability, conversion of apps as well as the company's overall brand image. Ratings are a key performance indicator of an app.   
   
From our research, we found that the average volume of ratings across all app categories is 4.17. The histogram plot is skewed to the right indicating that the majority of the apps are highly rated with only a few exceptions in the low-rated apps.
  
