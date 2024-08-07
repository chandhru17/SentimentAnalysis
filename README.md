# Sentiment Analysis Project

## Overview

This project aims to analyze sentiment in text data using various machine learning models. It leverages customer reviews from the Amazon dataset to classify reviews as positive or negative based on their overall rating.

## Dataset

- **Source:** Amazon Reviews Dataset
- **Features:**
  - `reviewText`: Text of the review.
  - `overall`: Overall rating of the review, converted to binary sentiment (positive if rating > 3, negative otherwise).

## Preprocessing

- **Text Cleaning:**
  - Fill missing values in the `reviewText` column.
  - Convert text to lowercase and remove punctuation (implicitly handled by TfidfVectorizer).

- **Feature Extraction:**
  - Use TfidfVectorizer to convert text data into numerical features, considering the top 1000 words and ignoring English stop words.

- **Data Splitting:**
  - Split the dataset into training and test sets (80-20 split).

- **Oversampling:**
  - Apply RandomOverSampler to handle class imbalance in both training and test sets.

## Models and Results

### 1. Logistic Regression

**Description:**
- Trained a Logistic Regression model on the resampled training data.
- Evaluated on resampled test data.

**Metrics:**
- Accuracy: 0.86
- Precision: 0.83
- Recall: 0.92
- F1 Score: 0.87

**Visualization:**
- Confusion Matrix to evaluate model performance.

### 2. Random Forest

**Description:**
- Trained a Random Forest Classifier with 100 estimators.
- Evaluated using a probability threshold of 0.7.

**Metrics:**
- Accuracy: 0.87
- Precision: 0.84
- Recall: 0.93
- F1 Score: 0.88

**Visualization:**
- Confusion Matrix to evaluate model performance.

### 3. Support Vector Machine (SVM)

**Description:**
- Trained an SVM with a linear kernel and C=1.0.
- Evaluated using a probability threshold of 0.6.

**Metrics:**
- Accuracy: 0.81
- Precision: 0.76
- Recall: 0.92
- F1 Score: 0.83

**Visualization:**
- Confusion Matrix to evaluate model performance.

### 4. Decision Tree

**Description:**
- Trained a Decision Tree Classifier on the resampled training data.
- Evaluated using a probability threshold of 0.6.

**Metrics:**
- Accuracy: 0.74
- Precision: 0.67
- Recall: 0.91
- F1 Score: 0.78

**Visualization:**
- Confusion Matrix to evaluate model performance.

### 5. Naive Bayes

**Description:**
- Trained a Multinomial Naive Bayes classifier on the resampled training data.
- Evaluated on resampled test data.

**Metrics:**
- Accuracy: 0.89
- Precision: 0.89
- Recall: 0.89
- F1 Score: 0.89

**Visualization:**
- Confusion Matrix to evaluate model performance.

## Conclusion

This project demonstrates the application of various machine learning algorithms to perform sentiment analysis on text data. Each model was evaluated based on accuracy, precision, recall, and F1 score, with visualizations provided through confusion matrices.

## Technologies Used

- **Programming Language:** Python
- **Libraries:**
  - `pandas`
  - `scikit-learn`
  - `imblearn`
  - `seaborn`
  - `matplotlib`


