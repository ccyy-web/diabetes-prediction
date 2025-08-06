##  Results

To evaluate model performance for diabetes classification, we implemented both a **single train-test split** and a **5-fold stratified cross-validation** strategy. The dataset was split into training and testing sets (80/20), and five classification models were tested:

- Logistic Regression (LR)
- Random Forest (RF)
- XGBoost
- Gradient Boosting Decision Tree (GBDT)
- Support Vector Machine (SVM)

###  Single Train-Test Split Evaluation

In the initial evaluation using a single hold-out set:

- **GBDT** achieved the best AUC of **0.831** and accuracy of **0.76**
- **XGBoost** and **Random Forest** also performed well with AUCs around **0.81**
- SHAP analysis was applied on the Random Forest model to enhance interpretability

| Model               | Accuracy | AUC       |
| ------------------- | -------- | --------- |
| Logistic Regression | 0.70     | 0.812     |
| Random Forest       | 0.78     | 0.819     |
| XGBoost             | 0.76     | 0.808     |
| GBDT                | 0.76     | **0.831** |
| SVM                 | 0.73     | 0.796     |



###  5-Fold Stratified Cross-Validation

To improve stability and reduce overfitting concerns, we applied **Stratified K-Fold Cross-Validation (k=5)**. This revealed more generalizable performance across models:

- **Logistic Regression** showed the most consistent and stable performance
- The average AUC of LR was **0.837**, slightly outperforming tree-based models in cross-validated settings

| Model               | Avg. Accuracy | Avg. AUC  |
| ------------------- | ------------- | --------- |
| Logistic Regression | **0.77**      | **0.837** |
| Random Forest       | 0.76          | 0.823     |
| GBDT                | 0.75          | 0.828     |
| XGBoost             | 0.74          | 0.796     |
| SVM                 | 0.75          | 0.822     |



###  Conclusion

While GBDT performed best in a single train-test evaluation, **Logistic Regression** demonstrated the highest overall robustness and generalizability during cross-validation. This suggests that simple models may still be highly effective for structured medical datasets like this one.