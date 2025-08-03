# Insurance Fraud Detection

[View the full notebook here](modeling-fraud-detection/Capstone_Fraud_Detection_Modeling.ipynb)

## Project Summary

Insurance fraud costs the industry billions of dollars each year. In this capstone project, I developed a tool that helps detect fraudulent insurance claims. By analyzing historical claim data, I built models that can highlight suspicious claims for further review. This can help insurers save money, reduce risk, and protect honest customers from premium increases.

---

## Key Insights from Data

Through exploring the data visually and statistically, I found several patterns linked to fraudulent claims:

- **Incident Types**: Single-vehicle and parked-car claims appear more likely to involve fraud.
- **Collision Types**: Cases with missing or unknown collision types are more common in fraudulent claims.
- **Incident Severity**: Higher severity claims (e.g., total vehicle loss) are more often linked to fraud.
- **Claim Amounts**: Fraudulent claims tend to have **significantly higher total claim amounts**.
- **Customer History**: Fraud is slightly more common among newer customers.
- **Occupation**: Certain jobs, like machine operators and clerical staff, appear more frequently in fraudulent cases.

These insights helped determine which variables are most useful in building a predictive model.

---

## What This Project Includes

- Cleaned and prepared dataset of insurance claims  
- Charts and visual comparisons of fraud patterns  
- Multiple fraud detection models (Logistic Regression, Random Forest, Gradient Boosting, SVM, KNN)  
- Hyperparameter tuning with Grid Search  
- Final model evaluation using metrics like F1-score and ROC AUC  

---

## Tools Used

- **Python** for data analysis and modeling
- **Pandas, NumPy** for data handling
- **Seaborn, Matplotlib, Plotly** for visualizations
- **Scikit-learn** for model building and evaluation
- **SMOTE** for handling class imbalance
- **GridSearchCV** for hyperparameter optimization

---

## Results

The Random Forest and Gradient Boosting models performed best, with the highest F1-scores and recall values. These models are better at catching fraudulent claims while minimizing false positives.

---

## Why This Matters

By identifying suspicious claims early, this solution can:
- Save insurers significant money
- Streamline investigations
- Protect honest policyholders from the effects of fraud

---

## Findings

Based on the visual exploration of key features found in my notebook:

#### Categorical Features
- **Incident Type**: Certain types, such as single-vehicle collisions, appear to have higher fraud rates.
- **Collision Type**: Rear-end collisions have the highest fraud rate, while sideswiped or front colisions still have relatively high fraud rates (Almost equal to non-fraud cases)
- **Incident Severity**: Incident Serverity of "Minor" and "Total Loss" have a ratio of fradulant cases to non-frudulant in about a 1:2 ratio.
- **Insured Occupation**: Some professions (e.g. Sales, Tech Support and Transport Moving) have a much higher fraud reporting than other profressions.
- **Authorities Contacted**: Fraud cases are more likely to involve situations where the police were the authorities contacted have the lowest amount of fradulant claims. This suggests that those who commit fraud will be less likely to contact the police during an incident.

#### Numerical Features

- **Total Claim Amount**:
Fraudulent claims have notably higher claim amounts.

* Median: $61,290 (fraud) vs. $56,520 (non-fraud)

* Max values are very similar, but fraud claims are skewed higher overall.

- **Age**:
* Little to no difference between fraud and non-fraud groups.

* Both have a median age around 38–39 years.

- **Months as Customer**:
* Slightly higher average for fraudulent claims.

* Mean: ~208 months (fraud) vs. ~202 months (non-fraud)

* Suggests fraud isn’t just a new-customer issue.

- **Policy Annual Premium**:
* No significant difference between fraud and non-fraud claims.

* Both groups center around $1,250/year.

---

## Next Steps

- Deploy the best-performing model for real-time claim screening
- Continuously update the model as new fraud trends appear
- Explore advanced anomaly detection methods for emerging fraud patterns
