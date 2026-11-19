# Google Play Store App Insights

This is an exploratory data analysis project on the Google Play Store dataset from Kaggle. I wanted to find out what makes an app successful on the Play Store by looking at ratings, reviews, installs, size, price and categories.

## Dataset

The project uses two files:

1. **googleplaystore.csv** with about 10,800 apps and details like category, rating, reviews, size, installs, price and last updated date.
2. **googleplaystore_user_reviews.csv** with about 64,000 user reviews and their sentiment.

## What I did

**Data cleaning.** I removed one broken row and dropped only exact duplicate rows, which left 10,357 rows. I converted Installs, Price, Reviews and Size into numbers and Last Updated into a date. Category and Genres were cleaned so the names are consistent. One missing Type was filled as Free since its price was 0. I left Rating empty where it was missing because most of those apps have no reviews, and filling them would give fake ratings. For questions about individual apps, like the top installed or most reviewed apps, I used one row per app so the same app does not show up twice.

**Analysis.** I answered 25 questions split into basic, medium and advanced levels. These cover average ratings, free vs paid apps, category performance, the effect of price and size, update trends, and sentiment analysis of user reviews using TextBlob.

## Key findings

Most apps are free (92.6%) and made for everyone, and the average rating is 4.19.

Game, Communication and Tools get the most installs.

Installs, price and size have only a small effect on ratings. Very expensive apps (over 50 dollars) are rated a bit lower.

Free apps get around 37 times more reviews than paid apps.

Users love apps that are easy to use, and their biggest complaints are crashes, bugs and bad updates.

## Tools used

Python, Pandas, NumPy, Matplotlib, Seaborn and TextBlob, all run on Kaggle.

## How to run

Open the notebook on Kaggle, add the Google Play Store dataset, and click Run All. The charts are saved in the images folder inside the working directory.
