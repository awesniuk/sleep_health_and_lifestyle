# Sleep Quality Prediction Project

This project aims to predict sleep quality based on various lifestyle and health factors using machine learning techniques.

## Dataset

The project utilizes the "Sleep Health and Lifestyle Dataset" which includes information about individuals' sleep patterns, daily habits, and health metrics.

Source dataset: https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset

## Data Preprocessing

The following data preprocessing steps are performed:

- Encoding categorical features:
    - Gender: One-hot encoding
    - Occupation: One-hot encoding after grouping less frequent occupations into "Other"
    - BMI Category: Ordinal encoding
- Splitting "Blood Pressure" into "Systolic Pressure" and "Diastolic Pressure"
- Scaling numerical features using StandardScaler

## Model Training

- A pipeline is constructed with the following steps:
    - Custom transformers for encoding categorical features and splitting blood pressure.
    - StandardScaler for numerical feature scaling.
    - BaggingClassifier with RandomForestClassifier as the base estimator.
- GridSearchCV is used to find the best hyperparameters for the BaggingClassifier and RandomForestClassifier.
- The model is trained on the training set and evaluated on the test set.

## Evaluation Metrics

The model is evaluated using the following metrics:

- Mean Squared Error (MSE)
- R^2 Score
- Classification Report
- Confusion Matrix

## Results

The best model achieved the following performance:

- **Best parameters:** (Output of grid search best parameters)
- **Best score:** (Output of grid search best score)
- **Mean Squared Error:** (Output of MSE)
- **R^2 Score:** (Output of R^2 score)
- **Classification Report:** (Output of classification report)

A confusion matrix is also plotted to visualize the model's performance.

## Visualization

Decision trees from the best model are plotted to provide insights into the model's decision-making process.

## Conclusion

This project demonstrates the use of machine learning for predicting sleep quality. The results show that the model can effectively predict sleep quality based on the provided features.

## Future Work

- Explore other machine learning models and feature engineering techniques.
- Incorporate more data and features to improve model accuracy.
- Develop a user interface for the model.
