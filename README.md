# Credit-Risk-Report
The purpose of this analysis was to build and evaluate a machine learning model that predicts the risk status of a loan—specifically, whether a loan is classified as "Healthy" or "High-Risk". The prediction model is intended to support financial institutions in quickly identifying potentially risky loans based on borrower financial metrics.
The dataset included key financial variables such as:
- `loan_size `
- `interest_rate`
- `borrower_income`
- `debt_to_income`
- `num_of_accounts`
- `derogatory_marks`
- `total_debt`
The target variable was `loan_status`, with the two classes being:
- **Healthy Loan:** 18,759 instances
- **High-Risk Loan:** 625 instances

This demonstrates a significant class imbalance (~97% Health vs. ~3% High-Risk).

The analysis followed these main stages:
1. Data preprocessing and cleaning.
2. Splitting the dataset into training and test sets.
3. Training a **LogisticRegression** model.
4. Generating predictions and evaluating performance using classification metrics.

## **Results**
Logistic Regression Model
- Accuracy: 0.99
- Precision:
  - Healthy Loan: 1.00
  - High-Risk Loan: 1.00
- Recall:
  - Healthy Loan: 1.00
  - High-Risk Loan: 0.95
- F1-Score:
  - Healthy Loan: 1.00
  - High-Risk Loan: 0.91

## **Summary**
Overall, the **LogisticRegression** model performed very well. It achieved perfect classification on the dominant healthy loan class, while also showing some strong metrics for the minority high-risk loan class, despite the observed imbalance.
- **Business Consideration**: In this case, correctly identifying **High-Risk Loans** is more critical than misclassifying a small number of Healthy Loans. Perhaps training the model on a more balanced dataset or trying to tune the model to catch more high-risk loans at the cost of a few healthy classifications could see improvements in this area. However, a 95% recall for High-Risk Loans seems to suggest that this model is sufficient at catching these high-risk cases.
- **Recommendation** Based on the high metrics observed, this Logistic Regression model is recommended for deployment in production environments. Depending on each use-case, the model could be tuned to further improve metrics within the high-risk loans class.
  
