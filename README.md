# Amazon Review Sentiment Analysis

This project involves sentiment analysis of Amazon product reviews using various text processing and machine learning techniques. The steps include data preprocessing, exploratory data analysis, sentiment analysis, and building machine learning models to classify sentiments as positive or negative.

## Table of Contents

- [Introduction](#introduction)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Sentiment Analysis](#sentiment-analysis)
- [Machine Learning Models](#machine-learning-models)
- [Usage](#usage)
- [Conclusion](#conclusion)

## Introduction

The goal of this project is to analyze Amazon product reviews and classify them as positive or negative. The analysis involves preprocessing the text data, visualizing word frequencies, performing sentiment analysis, and building machine learning models for classification.

## Data Preprocessing

1. **Loading Data**: The dataset is loaded from an Excel file.
2. **Text Normalization**:
   - Convert text to lowercase.
   - Remove punctuations and numbers.
   - Remove stopwords.
   - Remove rare words.
   - Lemmatize the text.
     
## Exploratory Data Analysis
Here, we perform some exploratory data analysis to visualize the word frequencies:
1. Word Frequency Bar Plot: Plotting words with frequency greater than 500.
2. Word Cloud: Visualization of word frequencies using a word cloud.

## Sentiment Analysis
In this step, we use the VADER sentiment analysis tool to label reviews as positive or negative:
1. Install NLTK and Download VADER Lexicon.
2. Perform Sentiment Analysis.

## Machine Learning Models
We build and evaluate machine learning models to classify sentiments:
1. Splitting Data into Train and Test Sets
2. TF-IDF Word Level Transformation
3. Logistic Regression Model
4. Random Forest Model

## Usage
Clone the repository.
Install the necessary dependencies.
Run the Jupyter notebook or the Python script to execute the analysis.

## Conclusion
This project demonstrates a complete workflow for sentiment analysis on Amazon product reviews, from data preprocessing and exploratory analysis to sentiment classification using machine learning models. Feel free to explore the code and modify it for your own data and use cases.


