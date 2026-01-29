# Company Bankruptcy Prediction

# Problem Statement
The objective of this project is to predict whether a company is at risk of bankruptcy using financial ratios and performance indicators. Early identification of financially distressed companies can help investors and lenders reduce financial risk.

---

# Business Context
Bankruptcy prediction is a **high-risk classification problem** where missing a bankrupt company (false negative) can be far more costly than incorrectly flagging a healthy company.  
Therefore, accuracy alone is not sufficient, and special attention must be given to **class imbalance and evaluation metrics**.

---

# Approach
- Framed the problem as a **binary classification task**
- Identified and handled **class imbalance** using SMOTE
- Standardized numerical features using `StandardScaler`
- Built a machine learning pipeline to prevent data leakage
- Performed **cross-validation** to ensure robust model evaluation
- Tuned hyperparameters using **RandomizedSearchCV**
- Selected the final model based on **Recall and F1-score**

---

# Models Used
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

---

# Validation Strategy
- Train-test split with stratification
- Stratified K-Fold Cross Validation
- Hyperparameter tuning with RandomizedSearchCV

---

# Evaluation Metrics
Due to class imbalance, the following metrics were prioritized:
- Recall
- F1-score
- Precision
- ROC-AUC
- Confusion Matrix

Accuracy was used only as a **secondary metric**.

---

# Tools & Libraries
- Python
- scikit-learn
- imbalanced-learn (SMOTE, Pipeline)
- pandas
- numpy
- matplotlib

---

# Key Insights
- Handling class imbalance significantly improved model recall
- Tree-based models captured non-linear financial risk patterns better
- Feature scaling improved the stability of Logistic Regression
- Recall–precision trade-off was carefully analyzed to reduce false negatives
