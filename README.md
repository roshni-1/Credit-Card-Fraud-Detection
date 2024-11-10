# Credit Card Fraud Detection Project

## Project Overview

This project focuses on detecting fraudulent credit card transactions using machine learning techniques. Due to the highly imbalanced nature of the dataset, where fraudulent transactions are significantly fewer than non-fraudulent ones, special methods were employed to balance the data and enhance the model's performance. An ensemble model was used to combine the strengths of multiple classifiers to improve the accuracy and reliability of fraud detection.

## Dataset

The dataset consists of credit card transactions, each labeled as either fraudulent or non-fraudulent. The primary challenge is the substantial imbalance between the two classes, with fraudulent transactions being very rare. Link to the dataset: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data

## Project Steps

### 1. Data Preparation

- **Data Cleaning**: Ensured that the dataset is free from any inconsistencies or missing values.
- **Feature Selection**: Selected relevant features that are most likely to help in detecting fraudulent transactions.
- **Data Balancing**: Used techniques like undersampling to balance the dataset due to the imbalanced nature of the data.

### 2. Feature Standardization

Standardized the features to ensure that they have a mean of 0 and a standard deviation of 1. This step is crucial for algorithms that rely on distance calculations.

