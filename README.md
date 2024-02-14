# Breast Cancer Prediction

## Abstract
Breast cancer is a significant health concern for women in the UK, often treated with chemotherapy. However, chemotherapy can be toxic and not always effective. Pathological complete response (pCR) is a critical indicator of treatment success, with higher pCR rates leading to better relapse-free survival (RFS). This project aims to predict PCR and RFS for breast cancer patients using clinical and MRI data. Various machine learning models are employed to analyze a dataset and identify the most accurate model. For the classification (pCR) task, the ANN model yielded the best results with a cross-validation score of 80%. For the regression (RFS) task, the ANN model yielded the best results with a mean absolute error of 21.28 in a 5-fold cross validation.


## 1. Introduction
This project focuses on predicting PCR and RFS outcomes for breast cancer patients by analyzing a dataset and training multiple machine learning models, providing a thorough exploration of methods and findings, leading to reliable models.

## 2. Data Pre-processing
Data pre-processing involved cleaning the dataset and handling missing values. Various techniques were employed, such as forward filling, mean imputation, K-nearest neighbors (KNN) imputation, and iterative imputation. Anomalies outside the 5th and 95th percentile were removed, and feature scaling was applied to standardize the data. One-hot encoding was used for the age attribute to reduce variance and improve model performance.

## 3. Feature Selection
Feature selection included visualizations to identify relevant features and correlations. Principal Component Analysis (PCA) was used to reduce dimensionality. Three wrapper methods—variance threshold, univariate feature selection, and mutual information feature selection—were employed to reduce feature dimensionality for the RFS task. SelectKBest with F_classif was used for feature selection in the pCR classification task.

## 4. Classification (PCR)
Four machine learning models were compared for predicting pCR: Logistic Regression, Support Vector Machine, Decision Tree, and Artificial Neural Network (ANN). These models were evaluated using classification accuracy, confusion matrices, and F1 score. The ANN model was chosen as it yielded the best results.

## 5. Regression (RFS)
Four regression models were compared for predicting RFS: Linear Regression, Support Vector Machine, Decision Tree, and ANN. Bayesian optimization was used to tune hyperparameters for the ANN. The ANN model was selected as it had the lowest mean absolute error and promising statistics.

## 6. Results
For the classification (PCR) task, the ANN model yielded the best results with a cross-validation score of 80%. For the regression (RFS) task, the ANN model yielded the best results with a mean absolute error of 21.28 in a 5-fold cross validation.

## 7. Conclusion
The project identified some challenges, including imbalanced data in the pCR classification task. Despite these challenges, the models showed promise, especially when training data was increased. Feature selection and hyperparameter tuning were also crucial in model performance. Future work may involve further research into the dataset to improve model accuracy and reliability.

In summary, this project offers a valuable step towards personalized breast cancer treatment, with the potential to predict chemotherapy patients outcomes and contribute to the field of oncology.
