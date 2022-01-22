
# Spotify Data Analysis


## Overview

![spotify](https://user-images.githubusercontent.com/89357104/147999820-7eac0382-2b34-476b-818e-85ff8c85c78f.jpeg)

The music business has gone through, several technology driven shakeups over the past 30 years. The days of ranking songs based on how well
an album or single sold, or how often it was requested on your local radio station is long gone. Music production has vastly changed too, 
with at home recording cheaper than ever, bringing studio level production to people's bedrooms, and social media acting as a primary source
of marketing, artists don't need to sign up for a label to get their music out to listeners. 

Streaming platforms are largely how music is listened to today. Spotify is a Swedish based media streaming platform, founded on 23 April 2006. 
It is the world's largest music streaming service provider, with over 381 million monthly active users, including 172 million paying subscribers, 
as of September 2021. Spotify streams internationally in over 180 countries as of October 2021. Platforms like Spotify allow almost anyone with 
a musical project to upload their art for everyone in the world to listen to. With so many users, artists, or even single songs, can rack up 
millions, even billions of listens, and Spotify keeps count of each one of them.

## Goal
But what makes a song a hit? It's a question many musicians have asked over the years. Using the dataset below we're hoping to share
some insight by exploring Spotify streaming data from 2016 to 2018.


## Description of Data Source
We'll be preforming our analysis, and answering our questions using these datasets, [Spotify's Worldwide Daily Song Ranking](https://www.kaggle.com/edumucelli/spotifys-worldwide-daily-song-ranking/data), and [Spotify Tracks DB](https://www.kaggle.com/zaheenhamidani/ultimate-spotify-tracks-db?select=SpotifyFeatures.csv) from Kaggle. 
We'll be looking at the features from the Spotify Tracks DB, such as track duration, energy, danceabilityand more, while comparing and contrasting 
to Spotify's Worldwide Daily Song Ranking stream count. We're expecting to find some predictive quality between at least one feature and total streams.



## Software Used
  * Database
     * PostgreSQL
  *
  * Machine Learning 
    * Random Forest
    
  * Analyzing Data
    * Pandas 
    * Numpy 
  * 
  * 

## Machine Learning Model

For our project, we are going to use Logistics Regression as a supervised machine learning model. Logistics regression uses classification as a method. Using this model, we will be able to predict whether a song will be popular based on its features. Based on multiple factors, our model predicts whether a song will be popular or not, including acoustics, danceability, duration_ms, energy, instrumentals, liveness, loudness, mode, speech, tempo, and valence.

Two sets of data will be created: a train dataset and a test dataset. Based on the training dataset, the model will be trained. To assess its performance, it will use the testing dataset while it learns. Our model cannot predict how well it will perform on unseen data, so we will not use the entire dataset. Instead, we will use the portion we have set aside.

We will assign the variable X to input variables, and use the to predict y, the output. The features (X) will be acousticnes, danceability, duration_ms, energy, instrumentalnes, liveness, loudness, mode, speechiness, tempo, valence and the target will be the column outcome, where 1- represents a popular song and 0-not popular.
After determining the X, y, we will split the dataset into training and testing sets: X_train, X_test, y_train, y_test = train_test_split(X, y, random_state=1, stratify=y)
As we train the model with the training data, we will create predictions for y-values by using the testing X values (X_test).
As we finish predicting the y values with the logistics regression model, we will determine the accuracy of the model, and then we will decide if any further models will be used to achieve better accuracy.

* ## Advantages
  - Logistics regression is one of the simplest machine learning algorithms and performs great training effieciency is some cases.
  - The prdicted parameters give inference about the importance of each feature.
  - This model gives well-calibrated probabilities outputs along with the classification results.

* ## Disadvantages
  - As logistics regression predicts probabilistic outcomes based on independent features on large datasets, this will lead to overfitting. Thus, the model and the training data may not be able to predict the test results accurately.
  - If the data is not linearly separable in higher dimensions, it requires the transformation of nonlinear features by increasing the number of features. This is      required since non-linear problems cannot be solved.
  - Complex relationships are difficult to capture.




## Presentation 

* Presentation Document: [Google Slide Presentation](https://docs.google.com/presentation/d/1kofNapJf18HnhgTNp6hX8VxUg7Z1qYCCVxNfF793xiA/edit#slide=id.g723630543_3_0)

## Work as a Team

Eventhough our goal as a team is to collaborate and help each other on the different tasks, we separated our role as:
* Square: [Brandon Turner](https://github.com/BrandonTur90) will be responsible for the respiratory
* Triangle: [Oluwatobiloba Oduntan](https://github.com/Tobi1018) will create a mockup of a machine learning model.
* Circle: [Roxhensa Kardhiqi](https://github.com/roxhensa02) will create a mockup of a database with a set of sample data, or even fabricated data
* X: [Shantal Jambotkar](https://github.com/shantaljambotkar) will decide which technologies will be used for each step of the project and she is working on the Jupiter Notebook and cleaning the data.

