# Credit Risk Classification

## Overview
This repository, **credit-risk-classification**, demonstrates the process of building a machine learning model to classify credit risk using logistic regression. The project focuses on predicting whether loans are 'healthy' (low risk) or 'high-risk' based on various financial features.

## Project Structure
- **credit-risk-classification/credit_risk_classification.ipynb**: Jupyter Notebook containing the complete code workflow, including data preprocessing, model training, evaluation, and results interpretation.
- **credit-risk-classification/Resources/lending_data.csv**: The dataset used for training and testing the model.

## Dataset
The dataset, `lending_data.csv`, includes the following columns:
- **loan_size**: Size of the loan
- **interest_rate**: Interest rate applied to the loan
- **borrower_income**: Income of the borrower
- **debt_to_income**: Debt-to-income ratio
- **num_of_accounts**: Number of financial accounts held by the borrower
- **derogatory_marks**: Number of derogatory marks on the borrower's credit
- **total_debt**: Total debt held by the borrower
- **loan_status**: The target variable indicating whether the loan is healthy (0) or high-risk (1)

## Process Outline
1. **Data Loading and Exploration**:
   - Load the `lending_data.csv` file using Pandas.
   - Inspect the data structure and initial statistics.

2. **Data Preprocessing**:
   - Separate the features (X) and the target variable (y).
   - Split the data into training and testing sets using `train_test_split` with a test size of 25% and `random_state=1`.

3. **Model Building**:
   - Import `LogisticRegression` from `sklearn`.
   - Instantiate and train the logistic regression model with the training data.

4. **Model Evaluation**:
   - Use the trained model to make predictions on the test data.
   - Evaluate performance using a confusion matrix and a classification report.

### Key Results
- **Confusion Matrix**:
  ```
  [[18658   107]
   [   34   585]]
  ```
- **Classification Report**:
  ```
               precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.95      0.89       619

    accuracy                           0.99     19384
   macro avg       0.92      0.97      0.94     19384
   weighted avg    0.99      0.99      0.99     19384
    ```




### Analysis
- The model achieves high accuracy (99%) and performs well in predicting healthy loans with high precision and recall.
- For high-risk loans, the recall is strong (0.95), indicating that most high-risk cases are identified, though the precision (0.85) shows some false positives.

### Recommendation:
Yes, I recommend the model for company use with the following considerations:

1. **Strengths**:  
   - The model achieves **99% accuracy**, meaning it performs very well overall.  
   - Its high recall of **0.95** for high-risk loans ensures that most high-risk loans are correctly identified, minimizing the chances of missing critical cases.

2. **Weaknesses**:  
   - The precision for high-risk loans is **0.85**, indicating that 15% of loans predicted as high-risk may actually be healthy. This could lead to unnecessary actions taken on loans mistakenly identified as high-risk.  

3. **Contextual Use**:  
   - If the company values identifying high-risk loans with minimal false negatives (missing high-risk loans), the model is a good fit.  
   - However, if precision is critical (e.g., reducing unnecessary interventions for loans incorrectly flagged as high-risk), further fine-tuning or an additional layer of decision-making might be necessary.

In conclusion, the model is reliable and suitable for deployment, especially if paired with monitoring and iterative improvements to handle the trade-off between precision and recall for high-risk loans.

## Made by
**Widchy Joachim - Data Analyst**

GitHub: [@widchy95](https://github.com/widchy95)

