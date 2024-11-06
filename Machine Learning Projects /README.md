# Handwritten Digit Recognition Project

## Project Overview

This project aims to build a machine learning model capable of recognizing handwritten digits with high accuracy. The purpose is to simulate real-world applications, preparing for data analysis tasks in future studies and careers. The project uses a multi-class classification approach, applying several machine learning models to classify each digit accurately.

## Table of Contents
- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Data](#data)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Modeling](#modeling)
  - [Support Vector Machine (SVM)](#support-vector-machine-svm)
  - [Logistic Regression](#logistic-regression)
  - [Random Forest](#random-forest)
- [Results](#results)
- [Conclusions](#conclusions)
- [Contributors](#contributors)

## Problem Statement

The objective of this project is to accurately classify handwritten digits using machine learning techniques, helping to understand data preprocessing, exploratory data analysis, model selection, and evaluation. This problem is tackled with various models, each evaluated to identify the best-performing model based on accuracy.

## Data

The dataset used is the well-known **zipcode dataset**:
- **Training Data**: 7,291 16x16 pixel grayscale images representing digits 0-9.
- **Test Data**: 2,007 similarly formatted grayscale images.
- **Source**: The dataset is hosted at Stanford University’s site and includes images normalized in size and centered to ensure consistency.

Links to data:
- [Training Data](https://hastie.su.domains/ElemStatLearn/datasets/zip.train.gz)
- [Test Data](https://hastie.su.domains/ElemStatLearn/datasets/zip.test.gz)
- [Dataset Description](https://hastie.su.domains/ElemStatLearn/datasets/zip.info.txt)

## Exploratory Data Analysis (EDA)

EDA was conducted to understand the dataset's distribution and key characteristics:
- **Digit Distribution**: A bar graph revealed balanced frequency across digit classes, which supports unbiased model training.
- **Heatmap Analysis**: Using seaborn, a heatmap of average pixel intensities helped highlight common features across the digits, aiding in identifying patterns that may be useful for classification.

## Modeling

Three models were implemented, each evaluated with relevant metrics and strategies:

### Support Vector Machine (SVM)
- **Strategy**: Explored both One-Versus-Rest (OvR) and One-Versus-One (OvO) methods.
- **Kernel**: Linear kernel used for computational efficiency.
- **Outcome**: The OvO strategy performed slightly better, achieving an accuracy of approximately 97.73%.

### Logistic Regression
- **Strategy**: Applied both OvR and OvO methods with a convergence threshold set to 1,000 iterations.
- **Outcome**: The model reached about 94.85% accuracy, showing consistency but with minor misclassifications among visually similar digits.

### Random Forest
- **Parameter Tuning**: Experimented with tree depths from 1 to 30, identifying 10 as the optimal depth.
- **Outcome**: High classification accuracy, though performance varied slightly across different digit classes.

## Results

The performance of each model was assessed based on accuracy and the confusion matrix:
- **Support Vector Machine (SVM)**: Best-performing model with 97.73% accuracy.
- **Logistic Regression**: Achieved 94.85% accuracy, showing some challenges with certain digit pairs.
- **Random Forest**: Effective at classifying simple digits but showed variability with more complex shapes.

## Conclusions

The SVM model with the OvO approach emerged as the best choice for this multi-class classification task. This model demonstrated a high level of precision and recall across digit classes, proving effective for digit recognition tasks. However, minor adjustments or more advanced algorithms could be explored to handle similar but visually complex digits more accurately.

## Contributors

- **Karla Lopez** - Machine Learning Foundations, CAI2100 C

## License

This project is open-source and available under the [MIT License](LICENSE).
