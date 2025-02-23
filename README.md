# Decision-Tree-Customer-Churn
A machine learning project to predict customer churn using decision tree and random forest classifiers. The project involves data pre-processing, feature engineering, model tuning using Optuna, and evaluation using precision, recall, and accuracy metrics. Aimed at helping businesses predict and reduce customer attrition.

## Overview
Customer churn is a critical challenge for businesses, particularly in the banking sector, where retaining customers is crucial for long-term profitability. This project aims to develop a predictive model that identifies customers likely to churn using Decision Tree and Random Forest classifiers.

To enhance model performance, Optuna was used for hyperparameter tuning, ensuring optimal decision boundaries. The results provide valuable insights into factors influencing churn, helping banks take proactive measures to retain high-value customers.

## Dataset
- **Source:** Bank Customer Churn Dataset
- **Total Records:** 10,000
- **Features:** 15 (Demographics, Banking Details, Customer Behaviour, Financial Information)
- **Target Variable:** Exited (1 = Churned, 0 = Retained)

## Key Features
- **Demographics:** Age, Gender, Location
- **Banking Details:** Credit Score, Balance, Tenure, Number of Products
- **Customer Behaviour:** Complaints, Satisfaction Score, Active Membership
- **Financial Information:** Estimated Salary, Card Type, Points Earned

## Data Pre-processing & Feature Engineering
To ensure model accuracy, the dataset was pre-processed by:
- Removing redundant columns (RowNumber, CustomerId, Surname)
- Handling missing values and duplicate records
- Encoding categorical variables (Location, Gender, Card Type)
- Scaling numerical features where necessary
- Splitting data into train (70%) and test (30%)

## Exploratory Data Analysis (EDA)
EDA was conducted to uncover patterns influencing customer churn:
- **Feature Distributions:** Analysed churn rates across various features
- **Correlation Matrix:** Identified relationships between variables

## Key Observations
- Customers with low satisfaction scores are highly likely to churn
- Active membership significantly reduces churn probability
- Customers with fewer banking products are more likely to leave

## Modelling Approach
- **Decision Tree Classifier:** Decision Trees were used as a baseline model, with hyperparameters tuned via Optuna.

- **Random Forest Classifier:** Random Forest, an ensemble method, was implemented to improve performance by reducing overfitting. Optuna was used to find the best combination of parameters.

## Model Evaluation & Results
Both models performed exceptionally well, with both models achieving equal results:
| Model | Precision | Recall | Accuracy |
|--------------|------------|--------|-----------|
| Decision Tree | 99.52% | 99.68% | 99.83% |
| Random Forest | 99.52% | 99.68% | 99.83% |

## Key Insights from Model
- Customer Complaints is the strongest predictors of churn
- Active members & multi-product users are less likely to leave
- Credit Score & Location have a lower impact than expected

## Business Recommendations
1. **Enhance Complaint Resolution Processes**
	- Implement faster response mechanisms for complaints.
	- Offer personalized solutions to dissatisfied customers.

2. **Encourage Multi-Product Usage**
	- Promote bundled banking services (e.g., pairing savings accounts with credit cards).
	- Educate customers on the benefits of multiple financial products to increase product subscription and usage.

3. **Increase Customer Engagement**
	- Encourage active usage of digital banking and transaction services.
	- Provide incentives for frequent banking activities (e.g., cashback, reward points).

4. **Improve Onboarding for New Customers**
	- Offer personalized welcome packages and advisory services.
	- Follow up with new customers to ensure satisfaction in the first 6 months.