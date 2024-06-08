# Tweet Sentiment Analysis
Sentiment Analysis over the Sentiment140 Dataset

# Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- Methodology
- Results

# Introduction
<div align="justify">
<p>
Sentiment analysis, also known as opinion mining, is a natural language processing (NLP) technique used to determine the sentiment or emotion expressed in a piece of text. In this project, we perform sentiment analysis on the Sentiment140 dataset, which is a collection of 1.6 million tweets labeled as positive or negative.</p>
<p>
  
<p>
The goal here is to build and evaluate models that can accurately classify the sentiment of tweets. To achieve this, we will preprocess the data, experiment with various machine learning algorithms, and evaluate their performance using standard metrics. This project provides insights into the challenges and methodologies of sentiment analysis, and the results can be applied to real-world scenarios where understanding public sentiment is crucial.  
</p>
</div>

# Dataset
<p align="justify"><a href="https://www.kaggle.com/datasets/kazanova/sentiment140">Sentiment140</a> is a widely used dataset for sentiment analysis tasks, particularly for social media text. It was created by Alec Go, Richa Bhayani, and Lei Huang and is designed to facilitate the training and evaluation of sentiment analysis models. The dataset is composed of 1.6 million tweets, each labeled as either positive or negative based on the presence of emoticons.</p>

## Description
- **Number of Tweets**: 1,600,000
  
- **Labels**: The dataset contains two sentiment labels:
  - **0**: Negative sentiment
  - **4**: Positive sentiment'
    
- **Attributes**:
  - **Polarity**: Sentiment label of the tweet (0 for negative, 4 for positive)
  - **ID**: The unique identifier for each tweet
  - **Date**: The date when the tweet was created
  - **Query**: The query used to gather the tweet (this is always "NO_QUERY" for this dataset)
  - **User**: The username of the user who posted the tweet
  - **Text**: The content of the tweet

## Preprocessing
<p align="justify">
Before using the dataset for training and evaluation, several preprocessing steps are typically performed:

- **Removing Emoticons**: The emoticons used for labeling are removed to prevent them from influencing the model.
- **Cleaning Text**: This includes lowercasing the text, removing URLs, user mentions, special characters, and extra whitespace.
- **Tokenization**: Splitting the text into individual words or tokens.
- **Vectorization**: Converting the tokens into numerical features using techniques such as TF-IDF (Term Frequency-Inverse Document Frequency).
</p>
