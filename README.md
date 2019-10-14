# Metis Project 2

**Project 2 in the Metis Data Science Bootcamp**

Problem statement: *Using information scraped from the web, can we build linear regression models from which we can learn about digital media viewership?*

I focused on trending YouTube channels (in the How-To & Tutorials category) to determine which factors can predict the popularity of a YouTube video, measured by its View Count. Using BeautifulSoup, I scraped YouTube video data on over 5,000 videos from 200 of the most popular channels. I looked at the following features:

1. Video Duration
2. Publishing Date
3. Title Length (word count)
4. Title Sentiment
5. Keywords
6. Family-Friendly
7. Listed in search results
8. View count of channel's previous video(s)\*
9. Like count of channel's previous video(s)\*
10. Dislike count of channel's previous video(s)\*

\* Looked at each user's previous 10 videos. Narrowed this down to looking at the most recent video and the 10th most recent video from the respective channel for each video.

I performed OLS Regression using StatsModels and LASSO Regression using Scikit-learn to eliminate the features with insignificant effects on the response variable by evaluating each feature's p-values from StatsModel and the coefficient assigned from the LASSO model

The final predictive model uses OLS Regression with an R^2 value of 0.680.

## Files

[`p02_Data_Scrape_and_Clean.ipynb`](p02_Data_Scrape_and_Clean.ipynb) shows the process to scrape and clean all of the YouTube video data

[`p02_EDA_and_Modeling.ipynb`](p02_EDA_and_Modeling.ipynb) shows the process of training various linear regression models and evaluating feature relationships and model performance

Slides can be found [here](https://www.slideshare.net/AlisonGlazer/metis-project-2-predicting-video-popularity-on-youtube)
