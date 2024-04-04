# Breast Cancer Prediction

## Description
Breast cancer is a significant health concern for women, often treated with chemotherapy. However, chemotherapy is not always effective. Pathological complete response (pCR) is an indicator of treatment success with high pCR rates leading to better relapse-free survival (RFS) which is the duration after treatment in which a patient remains free from any signs/symptoms that the cancer will return.

This project predicts pCR (classification task) and RFS (regression task) outcomes for breast cancer patients by analysing patients clinical and MRI data, pre-processing the dataset, conducting feature engineering, training various ML models, tuning the models hyperparameters, and evaluating the models using appropriate methods such as k-fold cross validation. A thorough exploration of methods and findings can be seen throughout. For the pCR predictions, the ANN model yielded the best results with a 5-fold cross validation score of 80% (very high accuracies in predicting non-returning cancers but low accuracies in predicting returning cancers as dataset was imbalanced causing results to also be imbalanced). For the RFS predictions, the ANN model yielded the best results with a mean absolute error of 21.28 in a 5-fold cross validation.

## Data Pre-processing
Data pre-processing involved cleaning the dataset and handling missing values. Imputations techniques are used including K-nearest neighbors (KNN) imputation, iterative imputation, forward filling, and mean imputation. Anomalies outside the 5th and 95th percentiles are removed, and feature scaling is applied to standardize the data. One hot encoding is also conducted.

## Feature Selection
Data is visualized to identify relevant features and correlations. Principal Component Analysis (PCA) is used to reduce dimensionality. Three wrapper methods including variance threshold, univariate feature selection, and mutual information feature selection are used to reduce dimensionality for the RFS task. Selecting the k-best attributes using ANOVA F-value scoring is used to select features in the pCR classification task.

## PCR (Classification Task)
Four ML models are trained to predict pCR. These are Artificial Neural Network, Support Vector Machine, Logistic Regression, and Decision Tree. They are evaluated using classification accuracy, confusion matrices, and F1 score.

## RFS (Regression Task)
Four regression models are compared for predicting RFS: Artificial Neural Network, Support Vector Machine, Linear Regression, Decision Tree. Bayesian optimization is used to tune hyperparameters for the ANN.

## Results
For the classification (pCR) task, the ANN model yielded the best results with a cross-validation score of 80%. For the regression (RFS) task, the ANN model yielded the best results with a mean absolute error of 21.28 in a 5-fold cross validation.

## Conclusion
For the regression task, the models yielded decent results. For the classification task however, the models yielded very high accuracies in predicting non-returning cancers but low accuracies in predicting returning cancers as the dataset was imbalanced causing the results to also be imbalanced. Future work may involve more research into the dataset to further improve the classification tasks models.

In summary, this project offers contribution towards breast cancer treatment and the field of oncology.
