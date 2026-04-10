## Fraud Detection Model Evaluation — Metrics that Matter

### Objective
Evaluate the performance of a logistic regression fraud detection model in a highly imbalanced setting, emphasizing decision-relevant metrics and threshold optimization over conventional accuracy.

---

### Methodology
- Utilized the Kaggle Credit Card Fraud Detection dataset (284,807 transactions; 0.172% fraud incidence), consisting of PCA-anonymized features (V1–V28), transaction amount, and a binary fraud indicator.  
- Established a naïve baseline classifier to demonstrate the **accuracy paradox**, highlighting the limitations of accuracy in rare-event classification.  
- Trained a logistic regression model and evaluated performance using:
  - Confusion matrices across multiple thresholds  
  - Precision, Recall, and F1-Score  
  - ROC curves and ROC-AUC  
  - Precision-Recall curves and PR-AUC  
- Conducted **threshold analysis** by varying classification cutoffs to quantify trade-offs between false positives and false negatives.  
- Incorporated an **operational constraint** (maximum of 500 investigations per day) to identify a feasible decision threshold aligned with real-world resource limitations.  
- Compared statistical performance metrics with business-oriented outcomes to bridge model evaluation and economic decision-making.

---

### Key Findings
- The naïve baseline achieved **99.83% accuracy while failing to detect any fraud**, illustrating the inadequacy of accuracy as a metric in severely imbalanced datasets.  
- Logistic regression produced a strong **ROC-AUC**, but more importantly, a meaningful **PR-AUC**, confirming its ability to identify rare fraud cases despite class imbalance.  
- The **optimal F1 threshold deviates significantly from the default 0.5**, demonstrating that standard classification rules are not appropriate in this context.  
- Introducing a **capacity constraint (≤500 flagged transactions)** shifts the optimal operating point, requiring a lower threshold to maximize fraud detection within operational limits.  
- Overall, model evaluation must be framed as a **decision problem**, where threshold selection reflects economic trade-offs between missed fraud (false negatives) and unnecessary investigations (false positives), rather than purely statistical fit.
