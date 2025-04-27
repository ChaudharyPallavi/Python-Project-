# Bank Customer Churn Prediction Model - Project Summary

## 1. Project Overview
In today's highly competitive banking environment, customer retention is more critical than ever.
This project focuses on predicting customer churn — identifying customers who are likely to leave the bank — enabling early intervention strategies to retain high-value customers and reduce revenue loss.
Using a dummy (synthetic) dataset that mirrors real-world banking scenarios, we conducted a complete data science lifecycle workflow:
- **Dataset Information**
- **Exploratory data analysis (EDA)**
- **Visualizations and Insights**
- **Model building and evaluation**

## 2. Dataset Information
Source: Synthetic bank customer dataset

Key Features:
- **Demographics**: Gender, Age, Geography
- **Bank info**: Credit Score, Balance, Tenure, NumOfProducts, IsActiveMember
- **Financials**: EstimatedSalary
- **Target**: Exited (1 = Customer left, 0 = Customer stayed)

## 3. Exploratory Data Analysis (EDA) Summary
**Data Cleaning:**
 - No missing values found.
 - Dropped unnecessary columns like RowNumber, CustomerId, and Surname.

**Key Observations:**

- **Gender**: Slightly more males than females, but churn rate higher among females.
- **Geography**:Customers from Germany showed a higher churn rate compared to France and Spain.
- **Age**:
  - Older customers have a higher tendency to churn
  - Customers aged 40+ are at significantly higher risk.
- **Balance:**
  - No clear direct correlation; even customers with zero balance churned.
  - Products and Activity:
    - Customers with only 1 product had a higher churn rate.
    - Inactive customers are more likely to churn.
- **Credit Score:**
    - Lower credit scores slightly correlate with higher churn, but not strongly.
- **Tenure:**
  - No strong relationship between tenure and churn detected.

 ## 4. Visualizations and Insights
- Churn Rate by Gender: higher churn among females.
- Churn Rate by Geography: Germany customers churn the most.
- Age Distribution: churn rate rises sharply after 40 years.
- Balance vs Churn: customers with both high and low balances have churned.
- IsActiveMember vs Churn: inactive members are much more likely to leave.
-(The visuals included bar plots, histograms, and countplots that clearly highlighted these insights.)

## 5. Model Building and Evaluation
**Preprocessing:**
- Categorical encoding for Geography and Gender.
- Standardization of numerical features using StandardScaler.
**Models Applied:**
- Logistic Regression
- Random Forest Classifier

**Best Performing Model:** Random Forest Classifier
- Random Forest Classifier Results:
 - Accuracy: ~86%
 - Precision: ~84%
 - Recall: ~57%
 - F1-Score: ~68%

**Confusion Matrix Insights:**
- High number of correctly classified customers.
- Moderate recall, indicating some churners still not captured (room for further improvement).

## 6. Final Conclusion
- The model, especially Random Forest Classifier , predicts churn with high accuracy.
-  Age, Geography, and IsActiveMember emerged as strong churn indicators.
- The bank (in a real scenario) could use these insights to focus on retaining older, inactive customers especially from Germany.
- The dummy dataset served well for simulation; applying the same workflow on real-world data would be the next logical step.
