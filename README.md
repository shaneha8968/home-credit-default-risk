# Home Credit Default Risk Prediction

## Project Overview
This project analyzes loan applicant data to identify patterns associated with loan repayment difficulties. Exploratory Data Analysis (EDA) and machine learning classification models are used to understand credit risk and predict potential loan defaulters.

## Problem Statement
Financial institutions need to assess the risk of loan applicants to reduce potential financial losses. The objective of this project is to analyze applicant information and historical credit data to predict whether an applicant may have difficulty repaying a loan.

## Objectives
- Perform Exploratory Data Analysis (EDA) to identify patterns in loan default behavior.
- Analyze applicant demographics, financial information, and historical credit records.
- Clean and preprocess data, handle missing values, and engineer relevant features.
- Build and compare machine learning classification models.
- Evaluate model performance using appropriate classification metrics.

## Dataset
The project uses the Home Credit Default Risk dataset, containing seven related datasets:

- `application_train.csv`
- `bureau.csv`
- `bureau_balance.csv`
- `POS_CASH_balance.csv`
- `credit_card_balance.csv`
- `previous_application.csv`
- `installments_payments.csv`

The main dataset contains **307,511 loan applications**.

**Target variable:**
- `0` – No recorded repayment difficulty
- `1` – Repayment difficulty

The target is imbalanced, with approximately 8.07% of applicants classified as defaulters.

## Tools and Technologies
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook
- Machine Learning and Exploratory Data Analysis

## Machine Learning Models
The following classification models were evaluated:

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier

Logistic Regression was selected based on its validation F1-score at a classification threshold of 0.6.

## Final Model Results

The selected Logistic Regression model was evaluated on a separate test dataset.

| Metric | Result |
|---|---:|
| Accuracy | 79.66% |
| ROC-AUC | 0.7554 |
| Defaulter Precision | 20.4% |
| Defaulter Recall | 52.3% |
| Defaulter F1-score | 29.3% |

The model identifies approximately 52% of actual defaulters in the test dataset. However, its relatively low precision indicates that many applicants flagged as potential defaulters are not actual defaulters. Therefore, further improvement is needed before real-world use.

## Key Insights from EDA
- Younger applicants showed higher repayment difficulty rates than older applicants.
- Lower external credit scores were associated with higher default rates.
- Applicants with previous loan refusals showed higher repayment difficulty rates.
- Applicants with late installment payments or overdue records generally showed higher default rates.
- Missing values and class imbalance were important challenges during analysis and model development.

## Project Files
- `home_credit_default_risk.ipynb` – Jupyter Notebook containing the analysis, feature engineering, model training, and evaluation.
- `project_report.pdf` – Detailed project report covering EDA, model comparison, results, and challenges.

## Challenges Faced
- Handling large datasets with different structures and levels of detail.
- Aggregating historical credit records for each applicant.
- Managing missing values and mixed data types.
- Addressing the imbalance between defaulters and non-defaulters.
- Comparing models and selecting a classification threshold using validation data.

## Conclusion
This project demonstrates an end-to-end credit risk analysis workflow, from data preparation and exploratory analysis to machine learning model evaluation. Logistic Regression achieved a ROC-AUC score of 0.7554 and a defaulter recall of approximately 52.3% on the test dataset. Further feature engineering, model tuning, and business-cost analysis would be required before deploying the model in a real lending environment.

**Note:** This project is for educational and analytical purposes and is not intended for direct use in real-world lending decisions.
