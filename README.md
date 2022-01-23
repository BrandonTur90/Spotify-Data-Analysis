
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

For our project, we are going to use Random Forest model. Random Forest model is a supervised machine learning algorithm that is constructed from decision tree algorithms. It utilizes ensemble learning, which is a technique that combines many classifiers to provide solutions to complex problems. Using this model, we will be able to predict whether a song will be popular based on its features. Based on multiple factors, our model predicts whether a song will be popular or not (if the streams will be above average of 345,717 streams or below), including acoustics, danceability, duration_ms, energy, instrumentals, liveness, loudness, mode, speech, tempo, and valence.

*Data Preprocessing*

The streams value helped us to binary group the data in to two groups where 1 is the group where the streams values are above the average number of 345,717 streams and the 0 group the number below the average. These groups will be our target where we will train and test the model based on the song's features:acoustics, danceability, duration_ms, energy, instrumentals, liveness, loudness,key, mode, speech, tempo, and valence.
However, our data set contains categorical values for the column key and mode. Therefore, we used Scikit-learn's LabelEncoder to transorf text into numerical data.

Two sets of data will be created: a train dataset and a test dataset. Based on the training dataset, the model will be trained. To assess its performance, it will use the testing dataset while it learns. Our model cannot predict how well it will perform on unseen data, so we will not use the entire dataset. Instead, we will use the portion we have set aside.

*Description of how data was split into training and testing sets*

We will assign the variable X to input variables, and use the to predict y, the output. The features (X) will be acousticnes, danceability, duration_ms, energy, instrumentalnes, liveness, loudness, mode, speechiness, tempo, valence and the target will be the column outcome, where 1- represents a popular song and 0-not popular.
After determining the X, y, we will split the dataset into training and testing sets: X_train, X_test, y_train, y_test = train_test_split(X, y, random_state=1, stratify=y)
As we train the model with the training data, we will create predictions for y-values by using the testing X values (X_test).
As we finish predicting the y values with the random forest model, we will determine the accuracy of the model, and then we will decide if any further models will be used to achieve better accuracy.

![Random Forest](https://github.com/BrandonTur90/Spotify-Data-Analysis/blob/main/Resources/Random%20forest%20clasifier.png?raw=true)

* ## Advantages of Random Forest model
  - It can perform both regression and classification tasks.
  - A random forest produces good predictions that can be understood easily.
  - It can handle large datasets efficiently.
  - The random forest algorithm provides a higher level of accuracy in predicting outcomes over the decision tree algorithm.

* ## Disadvantages of Random Forest model
  - When using a random forest, more resources are required for computation.
  - It consumes more time compared to a decision tree algorithm.
  - When used for regression they cannot predict beyond the range in the traning data, and they may over-fit data sets that are particularly noisy.

*Explanation of changes in model choice*

When we first started the project, our goal was to predict if a song was likely to win a grammy based on the song's features. However, due to lack of data we changed our target and we will predict if a song will be popular and will have high number of streams based on the features of the song.
Another challenge was on the machine learning model. We first used logistics regression model. Even though the testing accuracy score was 75% the classifier report and the confusion matrix gave us non-diserable result. Therefore, as our target was binary data set, we applied the supersived machine learning Random Forest model.

* Accuracy score is a way to validate the model's performance. On our model, we had a accuracy score of 83% which is a acceptable percantage. However, as our target is a binary dataset, we applied the confusion matrix parameter to determine precision of the model, which is a measure of positive predicted value (PPV) where we will se how reliable a positive classification it is.

* Additional tranining that will take on the future is to see if any Overfitting or Underfitting happened to the model.
Also, it will be a good idea to check if the model will be more successfull if we use different Random Forest Hyperparameters.
  


## Presentation 

* Presentation Document: [Google Slide Presentation](https://docs.google.com/presentation/d/1kofNapJf18HnhgTNp6hX8VxUg7Z1qYCCVxNfF793xiA/edit#slide=id.g723630543_3_0)

## Work as a Team

Eventhough our goal as a team is to collaborate and help each other on the different tasks, we separated our role as:
* Square: [Brandon Turner](https://github.com/BrandonTur90) will be responsible for the repository.
* Triangle: [Oluwatobiloba Oduntan](https://github.com/Tobi1018) will create a mockup of a machine learning model.
* Circle: [Roxhensa Kardhiqi](https://github.com/roxhensa02) will create a mockup of a database with a set of sample data, or even fabricated data
* X: [Shantal Jambotkar](https://github.com/shantaljambotkar) will decide which technologies will be used for each step of the project and she is working on the Jupiter Notebook and cleaning the data.

