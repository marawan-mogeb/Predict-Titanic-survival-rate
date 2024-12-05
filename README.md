
# README: Titanic Survival Prediction

## Overview
This project predicts passenger survival on the Titanic using a Random Forest Classifier. The dataset, available at [Titanic Dataset](https://github.com/datasciencedojo/datasets/blob/master/titanic.csv), includes information such as age, sex, class, and fare.

## Steps
1. **Data Preprocessing**:
   - Filled missing values for `Age` with the median.
   - Imputed missing values for `Embarked` with the mode.
   - Dropped unnecessary columns (`Cabin`, `Ticket`, `Name`, `PassengerId`).
   - Encoded categorical variables (`Sex`, `Embarked`) using `LabelEncoder`.

2. **Model Training**:
   - Split data into training (80%) and test (20%) sets.
   - Trained a `RandomForestClassifier` with 100 estimators.

3. **Evaluation**:
   - Achieved an accuracy of **82.1%** on the test set.
   - Precision, Recall, and F1-score metrics were computed.
   - Confusion matrix revealed correct and incorrect predictions.

## Key Results
- **Accuracy**: 82.1%
- **Classification Report**:
  ```
                precision    recall  f1-score   support

           0       0.83      0.88      0.85       105
           1       0.81      0.74      0.77        74

    accuracy                           0.82       179
   macro avg       0.82      0.81      0.81       179
weighted avg       0.82      0.82      0.82       179
  ```
- **Confusion Matrix**:
  ```
  [[92 13]
   [19 55]]
  ```

## Requirements
- Python 3.x  
- pandas, numpy, sklearn

## Insights
The model demonstrates good performance, especially for predicting non-survivors. Further improvements can be made by tuning hyperparameters or testing other models.
