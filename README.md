# Amazon Review Sentiment Analysis

This project involves sentiment analysis of Amazon product reviews using various text processing and machine learning techniques. The steps include data preprocessing, exploratory data analysis, sentiment analysis, and building machine learning models to classify sentiments as positive or negative.

## Table of Contents

- [Introduction](#introduction)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Sentiment Analysis](#sentiment-analysis)
- [Machine Learning Models](#machine-learning-models)
- [Usage](#usage)
- [Dependencies](#dependencies)

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

```python
# Load the dataset
df = pd.read_excel(r"C:\Users\dogan\OneDrive\Desktop\amazon.xlsx")

# Normalizing Case Folding
df["Review"] = df["Review"].str.lower()

# Punctuations
df["Review"] = df["Review"].str.replace("[^\w\s]", "")

# Numbers
df["Review"] = df["Review"].str.replace("\d", "")

# Stopwords
sw = stopwords.words("english")
df["Review"] = df["Review"].apply(lambda x: " ".join(x for x in str(x).split() if x not in sw))

# Rarewords / Custom Words
sil = pd.Series(" ".join(df["Review"]).split()).value_counts()[-1000:]
df["Review"] = df["Review"].apply(lambda x: " ".join(x for x in x.split() if x not in sil))

# Lemmatization
df["Review"] = df["Review"].apply(lambda x: " ".join([Word(word).lemmatize() for word in x.split()]))
