## Evaluation Metric Rationale

### Why Logistic Regression?

Logistic Regression was selected as the **baseline model** for this fraud detection task due to the following reasons:

- **Simplicity & Interpretability**:  
  Logistic Regression provides clear, interpretable coefficients, helping stakeholders understand which features most influence the likelihood of fraud.

- **Ideal for Binary Classification**:  
  The target variable (`fraud_reported`) is binary (Yes/No), which Logistic Regression is specifically designed to handle.

- **Baseline Benchmarking**:  
  It establishes a reliable, lightweight benchmark to compare against more advanced models like Random Forests or XGBoost.

- **Handles Class Imbalance with `class_weight='balanced'`**:  
  This is critical for fraud detection, where fraudulent claims make up a small portion of the dataset.

---

### Why These Evaluation Metrics?

Because the dataset is highly imbalanced (very few fraud cases), traditional accuracy can be misleading — a model that always predicts "Not Fraud" could still appear accurate. Therefore, we used the following metrics:

| Metric         | Purpose                                                                 |
|----------------|-------------------------------------------------------------------------|
| **Precision**  | Of all predicted fraud cases, how many were actually fraud? <br>Useful for reducing false accusations. |
| **Recall**     | Of all actual fraud cases, how many did we correctly identify? <br>Critical for ensuring fraud is not missed. |
| **F1 Score**   | Harmonic mean of precision and recall. <br>Balanced view of model performance under class imbalance. |
| **Confusion Matrix** | Visual breakdown of true vs. false positives and negatives, providing a holistic view of prediction quality. |

> Although accuracy was calculated, the primary focus was recall and F1 score, since these better reflect a model’s ability to detect rare but important fraudulent cases.

---
