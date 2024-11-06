# Fake News Detection with NLP

## Project Overview

This project builds a classifier to distinguish between fake and real news articles using Natural Language Processing (NLP). With a structured NLP pipeline, this project serves as a template for binary text classification tasks. Data preprocessing, feature extraction, and model building techniques are applied to identify fake news articles effectively.

This project was guided by Dr. Ernesto Lee's article, ["Zero to Hero in Natural Language Processing (NLP): A Beginner’s Template for Text Classification"](https://drlee.io/zero-to-hero-in-natural-language-processing-nlp-a-beginners-template-for-text-classification-73839ef3e2e7), which provides an excellent foundational template for text classification.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [NLP Pipeline Steps](#nlp-pipeline-steps)
  - [1. Loading and Understanding the Dataset](#1-loading-and-understanding-the-dataset)
  - [2. Data Preprocessing](#2-data-preprocessing)
  - [3. Text Vectorization](#3-text-vectorization)
  - [4. Train-Test Split](#4-train-test-split)
  - [5. Model Building and Evaluation](#5-model-building-and-evaluation)
  - [6. Confusion Matrix](#6-confusion-matrix)
  - [7. Adapting the Template](#7-adapting-the-template)
- [Conclusion](#conclusion)
- [Authors](#authors)
- [Acknowledgments](#acknowledgments)

## Dataset

- **Name**: [Fake and Real News Dataset](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)
- **Description**: A text dataset labeled as either “Fake” or “Real.”
- **Columns**:
  - **title**: Headline of the news article
  - **text**: Content of the article
  - **label**: Label indicating whether the news is "Fake" or "Real"
- **Use Case**: A binary classification task that offers rich textual data, allowing for practice in feature extraction and classification.

## NLP Pipeline Steps

### 1. Loading and Understanding the Dataset
We start by loading the dataset from Kaggle and exploring its structure, handling missing values and mapping labels:
- **Label Mapping**: "Real" as 1, "Fake" as 0.

### 2. Data Preprocessing
Text preprocessing enhances model performance. Applied techniques include:
- **Text Cleaning**: Converting text to lowercase, removing special characters, and standardizing formats.
- **Stop Words Removal**: Removing common words that don’t contribute meaningfully to classification.

### 3. Text Vectorization
To prepare the text data for machine learning, we apply **Term Frequency-Inverse Document Frequency (TF-IDF)**, which converts text into numerical features. This method assigns weights based on term frequency and uniqueness across documents, ensuring that common words like “the” and “and” don’t dominate the feature space. We set a limit of 5,000 features to balance between capturing important terms and maintaining computational efficiency.


### 4. Train-Test Split
To evaluate model performance, the dataset is split into training and testing sets, ensuring robust assessment. The training set is used to build the model, while the testing set helps evaluate its effectiveness on unseen data.

### 5. Model Building and Evaluation
Three classifiers are implemented and compared for this binary classification task:
- **Logistic Regression**: A straightforward, effective linear model.
- **Support Vector Machine (SVM)**: Known for its capability in high-dimensional spaces, especially effective for text data.
- **XGBoost**: A powerful gradient boosting algorithm, often yielding strong performance in classification.

Each model is evaluated on accuracy, precision, recall, and F1-score to determine its effectiveness in detecting fake news.

### 6. Confusion Matrix
To better understand model performance, a **confusion matrix** is used to visualize the classifier’s ability to distinguish between "Fake" and "Real" labels. The confusion matrix highlights areas where the model performs well and where it may need improvement.

### 7. Adapting the Template
This NLP pipeline can easily be adapted for other binary classification tasks. Key areas to adjust when using this template for different datasets include:
- **Dataset Exploration**: Each dataset has unique characteristics, so data preprocessing steps may need to be tailored accordingly.
- **Model Selection**: Experiment with different classifiers to see which performs best on the given data.
- **Evaluation Metrics**: Use metrics that best capture the specific goals and needs of the new classification task.

## Conclusion

This project demonstrates a systematic approach to building a fake news detection model using NLP techniques. The project’s template, inspired by Dr. Lee’s guide, can be applied to other classification tasks, offering a robust starting point for tackling NLP problems.

## Authors
- **Karla Lopez**

## Acknowledgments

- Special thanks to **Dr. Ernesto Lee** for the insightful article, ["Zero to Hero in Natural Language Processing (NLP): A Beginner’s Template for Text Classification"](https://drlee.io/zero-to-hero-in-natural-language-processing-nlp-a-beginners-template-for-text-classification-73839ef3e2e7), which served as a foundational guide for this project.
