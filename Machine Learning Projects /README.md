# Handwritten Digit Recognition Project

## Project Overview

This project focuses on developing a machine learning system capable of accurately recognizing and classifying handwritten digits. The dataset, curated by AT&T Research Labs for the U.S. Postal Service, contains 7,291 training images and 2,007 test images, each representing a digit as a 16x16 pixel grayscale image. This system aims to assist in digit recognition tasks, potentially automating processes requiring handwritten digit classification.

## Table of Contents
- [Project Overview](#project-overview)
- [Data](#data)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Models and Methodology](#models-and-methodology)
  - [Support Vector Machine (SVM)](#support-vector-machine-svm)
  - [Logistic Regression](#logistic-regression)
  - [Random Forest](#random-forest)
- [Findings and Conclusions](#findings-and-conclusions)
- [Results](#results)
- [Contributors](#contributors)

## Data

The dataset includes:
- **Training Images**: 7,291 grayscale images, 16x16 pixels each
- **Test Images**: 2,007 grayscale images, 16x16 pixels each
- **Preprocessing**: Images are normalized for size and centered for uniformity.

## Exploratory Data Analysis (EDA)

EDA provided insights into the distribution and characteristics of the dataset:
- **Digit Distribution**: The dataset is balanced across all digits, enhancing model training reliability.
- **Heatmap Analysis**: A heatmap of average pixel intensities highlights common features across handwritten digits, aiding model accuracy by identifying distinct digit patterns.

## Models and Methodology

Three models were explored in this project:

### Support Vector Machine (SVM)
- **Approach**: Both One-Versus-Rest (OvR) and One-Versus-One (OvO) strategies were implemented.
- **Kernel**: Linear kernel for computational efficiency.
- **Performance**: OvO strategy showed a slightly better balance in precision and recall, achieving an accuracy of approximately **97.73%**.

### Logistic Regression
- **Approach**: Applied both OvR and OvO strategies with a convergence threshold of 1,000 iterations.
- **Performance**: Achieved an accuracy of approximately **94.85%**, with strong performance but occasional misclassifications among visually similar digits (e.g., ‘3’, ‘5’, and ‘8’).

### Random Forest
- **Parameter Tuning**: Tested maximum tree depths from 1 to 30, optimizing performance without overfitting.
- **Performance**: Demonstrated strong classification capability, especially for simpler digits, but slightly lower precision for complex shapes. Depth of 10 was found to be optimal.

## Findings and Conclusions

Through this project, the following insights were gained:
- **SVM**: Best-performing model, particularly with the OvO approach.
- **Logistic Regression**: Showed strong accuracy, though struggled slightly with visually similar digits.
- **Random Forest**: Effective for most classes but prone to slight inaccuracies with complex shapes.

Overall, SVM with OvO was identified as the most effective model for this digit recognition task.

## Results

| Model                | Accuracy |
|----------------------|----------|
| Support Vector Machine (OvO) | 97.73%  |
| Logistic Regression (OvO)    | 94.85%  |
| Random Forest                | Varies by depth (optimal ~95%) |

## Contributors
- **Karla Lopez** - Machine Learning Foundations, CAI2100 C

## License

This project is open-source and available under the [MIT License](LICENSE).
