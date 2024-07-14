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

### 3. Model Initialization

Initialized three different models to be used in the ensemble:
- **Label Spreading**: A semi-supervised learning algorithm that spreads the labels among the data points based on their similarity.
- **Label Propagation**: Similar to Label Spreading, this semi-supervised algorithm uses a graph-based method to propagate labels.
- **XGBoost Classifier**: A powerful supervised learning algorithm known for its high performance and accuracy in classification tasks.

### 4. Ensemble Model

Created an ensemble model using the three initialized classifiers. The ensemble method used is Voting Classifier, which combines the predictions from multiple models to make a final prediction. Soft voting was used to get probability outputs from each model, allowing for more nuanced decision-making.

### 5. Hyperparameter Tuning

Performed hyperparameter tuning using GridSearchCV to find the best parameters for each of the models in the ensemble. This step is essential to optimize the model's performance.

### 6. Model Training

Trained the ensemble model on the standardized training data. The model was trained to recognize patterns and distinguish between fraudulent and non-fraudulent transactions.

### 7. Predictions and Threshold Adjustment

Made predictions on the test data using the trained ensemble model. Adjusted the classification threshold to balance the precision and recall, aiming for optimal fraud detection performance.

### 8. Model Evaluation

Evaluated the model's performance using metrics like confusion matrix, precision, recall, and F1-score. These metrics help in understanding how well the model is distinguishing between fraudulent and non-fraudulent transactions.

## Results

The ensemble model showed high accuracy in detecting fraudulent credit card transactions. By adjusting the classification threshold, the model's performance was further optimized, achieving a good balance between precision and recall. The final model successfully identifies fraudulent transactions with a high degree of accuracy, demonstrating the effectiveness of the ensemble approach in handling imbalanced datasets.

## Conclusion

This project demonstrates the successful application of an ensemble model in detecting credit card fraud. The combination of semi-supervised learning algorithms and a supervised classifier, along with proper data balancing and threshold adjustment, resulted in a highly accurate fraud detection system. This approach can be applied to other imbalanced classification problems, showcasing the versatility and robustness of the methods used.
