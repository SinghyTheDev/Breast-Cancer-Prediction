# Breast Cancer Prediction

## Introduction
Breast cancer is a significant health concern for women, often treated with chemotherapy. However, chemotherapy is not always effective and can also be toxic. Pathological complete response (pCR) is an indicator of treatment success with high pCR rates leading to better relapse-free survival (RFS), which is the duration after treatment in which a patient remains free from any signs/symptoms of the cancer returning.

This project predicts pCR (classification task) and RFS (regression task) outcomes for breast cancer patients by analysing a dataset holding patients clinical and MRI data, pre-processing the dataset, conducting feature selection, training various ML models, tuning the models hyperparameters, and evaluating the models using appropriate methods such as k-fold cross validation, F1 score, and confusion matrices. This project leads to reliable models, and a thorough exploration of methods and findings can be seen throughout. For the pCR predictions, the ANN model yielded the best results with a 5-fold cross validation score of 80%. For the RFS predictions, the ANN model yielded the best results with a mean absolute error of 21.28 in a 5-fold cross validation.

## Data Pre-processing
Data pre-processing involved cleaning the dataset and handling missing values. Imputations techniques are used including K-nearest neighbors (KNN) imputation, iterative imputation, forward filling, mean imputation. Anomalies outside the 5th and 95th percentiles are removed, and feature scaling is applied to standardize the data. One hot encoding is also conducted.

## Feature Selection
Data is visualised to identify relevant features and correlations. Principal Component Analysis (PCA) is used to reduce dimensionality. Wrapper methods such as variance threshold, univariate feature selection, and mutual information feature selection are used to reduce dimensionality for the RFS task. Selecting the k-best attributes using ANOVA F-value scoring is used to select features in the pCR classification task.

## PCR (Classification Task)
Four ML models are trained to predict pCR. These are Artificial Neural Network, Logistic Regression, Support Vector Machine, and Decision Tree. They are evaluated using classification accuracy, confusion matrices, and F1 score. The ANN model is recommended as it yields the best results.

## RFS (Regression Task)
Four regression models are compared for predicting RFS: Artificial Neural Network, Linear Regression, Support Vector Machine, Decision Tree. Bayesian optimization is used to tune hyperparameters for the ANN. The ANN model is the recommended model as it yields the lowest mean absolute error.

## Results
For the classification (PCR) task, the ANN model yielded the best results with a cross-validation score of 80%. For the regression (RFS) task, the ANN model yielded the best results with a mean absolute error of 21.28 in a 5-fold cross validation.

## Conclusion
The models show promise, especially as training data is increased. Feature selection and hyperparameter tuning were crucial in model performance. Future work may involve more research into the dataset to further improve the models accuracy and reliability as there was some imbalanced data for the pCR task.

In summary, this project offers effective contribution towards breast cancer treatment and the field of oncology.
