# Breast Cancer Prediction

## Abstract
Breast cancer is a significant health concern for women, often treated with chemotherapy. However, chemotherapy is not always effective and can also be toxic. Pathological complete response (pCR) is an indicator of treatment success, with high pCR rates leading to better relapse free survival (RFS). This project predicts pCR (classification task) and RFS (regression task) for breast cancer patients using a dataset containing clinical and MRI data. Various ML models are implemented and their hyperparameters are tuned. For the pCR predictions, the ANN model yielded the best results with a 5-fold cross validation score of 80%. For the RFS predictions, the ANN model yielded the best results with a mean absolute error of 21.28 in a 5-fold cross validation.

## Introduction
This project focuses on predicting pCR and RFS outcomes for breast cancer patients by analysing a dataset and training various ML models. A thorough exploration of methods and findings can be seen throughout and leads to reliable models.

## Data Pre-processing
Data pre-processing involved cleaning the dataset and handling missing values. Various techniques are used such as forward filling, mean imputation, K-nearest neighbors (KNN) imputation, and iterative imputation. Anomalies outside the 5th and 95th percentile are removed, and feature scaling is applied to standardize the data. One hot encoding is used for the age attribute.

## Feature Selection
Feature selection starts with visualisations to identify relevant features and correlations. Principal Component Analysis (PCA) is used to reduce dimensionality. Three wrapper methods — variance threshold, univariate feature selection, and mutual information feature selection are used to reduce dimensionality for the RFS task. Select k best with ANOVA F-value scoring was used for feature selection in the pCR classification task.

## Classification (PCR)
Four ML models were compared for predicting pCR: Artificial Neural Network, Logistic Regression, Support Vector Machine, and Decision Tree. These models were evaluated using classification accuracy, confusion matrices, and F1 score. The ANN model was chosen as it yielded the best results.

## Regression (RFS)
Four regression models were compared for predicting RFS: Artificial Neural Network, Linear Regression, Support Vector Machine, Decision Tree. Bayesian optimization was used to tune hyperparameters for the ANN. The ANN model is the recommended model as it had the lowest mean absolute error.

## Results
For the classification (PCR) task, the ANN model yielded the best results with a cross-validation score of 80%. For the regression (RFS) task, the ANN model yielded the best results with a mean absolute error of 21.28 in a 5-fold cross validation.

## Conclusion
The models show promise, especially as training data is increased. Feature selection and hyperparameter tuning were crucial in model performance. Future work may involve further research into the dataset to improve model accuracy and reliability as there was some imbalanced data for the pCR classification task.

In summary, this project offers contribution towards breast cancer treatment and the field of oncology.
