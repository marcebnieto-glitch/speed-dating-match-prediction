# Speed Dating — Match Prediction with ML Classification Models
 
Machine learning project to predict whether two people will match in a speed dating event.
 
## Objective
Build a classification model that predicts if two participants will make a **match**, based on personal characteristics, mutual evaluations, and shared interests.
 
## Dataset
Speed Dating Experiment dataset from Kaggle — collected from real speed dating events including ratings on attractiveness, sincerity, intelligence, fun, ambition, and shared interests from both participants.
 
[Dataset source](https://www.kaggle.com/datasets/annavictoria/speed-dating-experiment)
 
## What's covered
 
**1. Data Preprocessing**
- Feature selection from 195 variables down to the most relevant ones
- Missing value treatment by variable type (median imputation, zero-fill, "unknown" category)
- Duplicate removal and column renaming for clarity
**2. Exploratory Data Analysis (EDA)**
- Distribution of matches vs. non-matches (class imbalance analysis)
- Visualization of null values by variable
- Correlation between personal attributes and match outcome
**3. Machine Learning — Binary Classification**
 
Four models compared to predict match (1) vs. no match (0):
 
| Model | Accuracy | Recall (match) | F1-score (match) |
|---|---|---|---|
| Logistic Regression (balanced) | 0.75 | **0.79** | 0.51 |
| SVM | 0.73 | 0.76 | 0.48 |
| XGBoost | 0.79 | 0.75 | 0.54 |
| Random Forest | 0.86 | 0.22 | 0.34 |
 
**Best model:** Logistic Regression with `class_weight='balanced'` — best recall for the minority class (match), which is the key metric for this problem.
 
**Class imbalance handling:** `class_weight='balanced'` and `scale_pos_weight` (XGBoost)
 
## Tools & Libraries
- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (Logistic Regression, SVM, Random Forest)
- XGBoost
## Key Findings
- Attractiveness and shared interests are the strongest predictors of a match
- High accuracy alone is misleading due to class imbalance — recall on the match class is the relevant metric
- Logistic Regression outperforms more complex models when optimized for recall
## Team project
Developed as part of the Master in Data Analytics for Business — UPF Barcelona School of Management.
 
