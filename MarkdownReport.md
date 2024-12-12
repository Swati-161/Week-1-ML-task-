```
# Credit Card Fraud Detection - Markdown Report

## Approach

1. **Data Preprocessing**:
   - Handled missing values by filling them with the median.
   - Removed duplicates to ensure data integrity.
   - Applied **log transformation** to the `Amount` feature to handle outliers.
   - Scaled features like `Log_Amount` and `Time` using **StandardScaler**.
   - Applied **SMOTE** to balance the class distribution between fraudulent and non-fraudulent transactions.

2. **Feature Engineering**:
   - Created new features like `Log_Amount` and `Log_Amount_Time_interaction` to provide better insights.
   - Calculated VIF to address multicollinearity.

3. **Model Training**:
   - Used **Logistic Regression** due to its simplicity for binary classification problems.
   - Trained the model on the resampled dataset (after SMOTE).

## Challenges

Several challenges were encountered during the course of the project:

1. **Class Imbalance**:
   - The dataset had a highly imbalanced distribution between fraudulent and non-fraudulent transactions. This could lead to poor performance of the model, as it may bias predictions toward the majority class.
   
2. **Feature Scaling**:
   - Scaling features like `Amount` and `Time` was essential to ensure that all features contribute equally to the model. Otherwise, the model could give more weight to higher-value features, which would be detrimental.
   
3. **Model Convergence Warning**:
   - The Logistic Regression model initially faced convergence issues during training due to the large number of iterations required for the solver to find an optimal solution.
   
## Results

The Logistic Regression model performed well, achieving the following metrics:

- **Accuracy**: 98%
- **Precision (Fraud Class)**: 99%
- **Recall (Fraud Class)**: 97%
- **F1-score**: 98%

```


