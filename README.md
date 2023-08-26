

# fars
To assess model performance, various classifiers are used to predict the categories of records within the FARS dataset.

EDA:
The dataset includes 100968 samples.
The dataset is mainly comprised of categorical data with age being the sole discrete value. While most features exhibit symmetric distributions with minimal skewness, there is an unusual outlier with a maximum period of 99.

The dataset exhibits an imbalance in terms of the target variable, potentially leading the model to excel at predicting the majority class while struggling with the minority class. To address this issue and enhance overall performance, the SMOTE sampling technique is applied, augmenting the minority class samples to improve the accuracy, precision, and recall of the model.

The standard scaler approach is used to normalize the variance of the characteristics. Because the dataset values differ on a greater scale, a standard scaler is required


Conclusion

All the models performed remarkably well, with Random Forest outperforming the others in terms of accuracy for the FARS dataset. Below are the accuracy results for different classifiers:

- Logistic Regression: 66%
- KNN without SMOTE: 70%
- KNN with SMOTE: 88%
- Decision Tree: 88%
- Random Forest: 90%

The use of SMOTE significantly improved accuracy across all models in predicting the eight different class labels. However, despite Random Forest achieving a very high accuracy score, I favor KNN over Random Forest due to Random Forest's accuracy dropping to 45% during cross-validation for a specific test data sample.
