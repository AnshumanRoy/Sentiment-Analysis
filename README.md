# Tweet Sentiment Analysis
Evaluation and comparison of models for the purpose of sentiment analysis over the Sentiment140 dataset.

# Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)

<a name="introduction"></a>
# Introduction
<p align="justify">
Sentiment analysis, also known as opinion mining, is a natural language processing (NLP) technique used to determine the sentiment or emotion expressed in a piece of text. In this project, we perform sentiment analysis on the Sentiment140 dataset, which is a collection of 1.6 million tweets labeled as positive or negative.
</p>

| Positive Sentiment Word Cloud              | Negative Sentiment Word Cloud               |
| ---------------------- | ---------------------- |
| ![positive word cloud](https://github.com/AnshumanRoy/Sentiment-Analysis/assets/56593553/d2cb50a8-a37f-4023-99e4-6bbf26112ddb) | ![negative word cloud](https://github.com/AnshumanRoy/Sentiment-Analysis/assets/56593553/7a5fee52-2a38-4c4f-ad8d-634c953da734) |

<p align="justify">
The goal here is to build and evaluate models that can accurately classify the sentiment of tweets. To achieve this, we will preprocess the data, experiment with various machine learning algorithms, and evaluate their performance using standard metrics. This project provides insights into the challenges and methodologies of sentiment analysis, and the results can be applied to real-world scenarios where understanding public sentiment is crucial.  
</p>

<a name="dataset"></a>
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
Before using the dataset for training and evaluation, several preprocessing steps were performed:

- **Convert Text to Lowercase**: All text in the dataset is converted to lowercase to ensure uniformity.
- **Remove Stopwords**: Common stopwords are removed from the text to reduce noise.
- **Remove Punctuations**: Punctuation marks are removed from the text.
- **Remove Repeating Characters**: Repeating characters in words are replaced with a single instance of that character.
- **Remove URLs**: URLs are removed from the text.
- **Remove Numbers**: Numerical digits are removed from the text.
- **Tokenize Text**: The text is tokenized into individual words.
- **Stemming**: Stemming is applied to reduce words to their root forms.
- **Lemmatization**: Lemmatization is applied to reduce words to their base or dictionary form.
</p>

<a name="methodology"></a>
# Methodology

The task here is to classify the tweets into two sentiment classes i.e. positive and negative. For this purpose, we have considered three models:
- **Bernoulli Naive Bayes Classifier**
- **Support Vector Machine (SVM) Model**
- **Logistic Regression Model**

## Transformation

<p align="justify">
The text was vectorized using a TF-IDF Vectorizer. This vectorizer enabled the conversion of raw text data into a numerical format suitable for machine learning algorithms. The <b>TF-IDF (Term Frequency-Inverse Document Frequency)</b> technique, implemented by the vectorizer, is particularly beneficial for sentiment analysis tasks. By considering both the frequency of terms in a document <b>(TF)</b> and the rarity of those terms across all documents <b>(IDF)</b>, <b>TF-IDF</b> captures the importance of words in distinguishing sentiment nuances. Unigrams and bigrams in the text were considered and the maximum number of features were limited to 500,000, ensuring efficient processing and representation of the text data.
</p>

## Evaluation

<p align="justify">
The model evaluation process includes computing evaluation metrics like <b>precision</b>, <b>recall</b>, and <b>F1-score</b>. Additionally, a <b>Confusion Matrix</b> is generated and visualized using a heatmap to assess the model's performance in classifying sentiments as negative or positive.
</p>

<p align="justify">
Furthermore, an <b>ROC curve</b> is plotted to analyze the model's <b>True Positive Rate (sensitivity)</b> against the <b>False Positive Rate (1 - specificity)</b> across various threshold values. The <b>Area Under the ROC Curve (AUC-ROC)</b> is calculated to quantify the model's discriminative power and overall performance.
</p>

<a name="results"></a>
# Results

|Model|Precision|Recall|F1-Score|Confusion Matrix|ROC Curve|
|-----|---------|------|--------|----------------|---------|
|<b>Bernoulli Naive Bayes Classifier</b>|0.80|0.80|0.80|<image src="https://github.com/AnshumanRoy/Sentiment-Analysis/assets/56593553/2bb58de6-188a-48aa-89d3-9daa5ebb9ecc" height=250px width=100%>|<image src="https://github.com/AnshumanRoy/Sentiment-Analysis/assets/56593553/d03c695a-b03c-4fc7-b458-c5c8f3d29f8c" height=250px width=100%>|
|<b>Support Vector Machine (SVM) Model</b>|0.81|0.81|0.81|<image src="https://github.com/AnshumanRoy/Sentiment-Analysis/assets/56593553/8a458af5-0fa7-4868-a449-ce81979d1d69" height=250px width=100%>|<image src="https://github.com/AnshumanRoy/Sentiment-Analysis/assets/56593553/89731d86-ccb7-4e4c-91b9-b8f4104695c6" height=250px width=100%>|
|<b>Bernoulli Naive Bayes Classifier</b>|0.83|0.83|0.83|<image src="https://github.com/AnshumanRoy/Sentiment-Analysis/assets/56593553/c2b85aab-3481-4176-bfa5-c40b2fd26d79" height=250px width=100%>|<image src="https://github.com/AnshumanRoy/Sentiment-Analysis/assets/56593553/ad153e69-f5b7-4a99-9503-39d204c621bf" height=250px width=100%>|
