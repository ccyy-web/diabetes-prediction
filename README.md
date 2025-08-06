# Diabetes Prediction using Machine Learning

This project uses the PIMA Indian Diabetes dataset to predict whether a patient is likely to have diabetes using various machine learning models.

## Dataset

- Public dataset with 768 samples and 8 clinical features.
- Includes features like glucose, BMI, age, blood pressure, etc.

## Exploratory Data Analysis (EDA)

- Violin plots for feature distribution
- Correlation heatmap
- Summary statistics

## Models Used

- Logistic Regression
- Random Forest
- XGBoost
- Gradient Boosting (GBDT)
- K-Nearest Neighbors (KNN)

## Evaluation

- Accuracy, Precision, Recall, F1-score
- AUC-ROC curves
- Confusion Matrix
- Model comparison bar chart

## Results

- Best model: Logistic Regression
- Accuracy: ~77%
- AUC: ~0.836
- PS：We evaluated multiple classification models using both train-test split and 5-fold stratified cross-validation. While Gradient Boosting Decision Tree (GBDT) achieved the highest AUC in a single run (0.83), Logistic Regression showed the most stable performance across all folds, with an average AUC of 0.836 and accuracy of 0.77. The results suggest LR is more generalizable under varying data splits.

## Tools

- Python
- pandas, numpy, matplotlib, seaborn
- scikit-learn, xgboost

## Author

- C