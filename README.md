# Bankruptcy Prevention – Predictive Classification Model

## Problem Statement & Business Objectives

Bankruptcy is one of the most serious risks a company can face. Early identification of companies at high risk of bankruptcy allows stakeholders (banks, investors, creditors, auditors, regulators) to take preventive actions, minimize financial losses, and support turnaround efforts.

**Business Objective**  
Develop a **binary classification model** that predicts whether a company is likely to go bankrupt (or remain non-bankrupt) based on six key risk and strength indicators.  
The solution should:  
- Achieve high predictive accuracy and reliability  
- Help reduce financial risk exposure for lending institutions and investors  
- Enable proactive monitoring and early warning systems  
- Be deployable as a user-friendly application (Flask / Streamlit) for practical business use  

**Acceptance Criterion** (as stated in project):  
End-to-end results must be deployable using Flask, Streamlit, or similar web framework.

## Abstract

This is a **supervised binary classification** project aimed at modeling the probability of business bankruptcy using six explanatory variables collected from 250 companies.

The dataset contains compact, interpretable features — all scored on a 0–0.5–1.0 scale — representing different dimensions of company health:

- **industrial_risk**          (0 = low, 0.5 = medium, 1 = high)  
- **management_risk**         (0 = low, 0.5 = medium, 1 = high)  
- **financial_flexibility**   (0 = low, 0.5 = medium, 1 = high)  
- **credibility**             (0 = low, 0.5 = medium, 1 = high)  
- **competitiveness**         (0 = low, 0.5 = medium, 1 = high)  
- **operating_risk**          (0 = low, 0.5 = medium, 1 = high)  

**Target variable**: class (bankruptcy = 1 / non-bankruptcy = 0)

The project follows a standard machine learning pipeline:  
- Exploratory Data Analysis (EDA) & visualization  
- Data preprocessing & feature understanding  
- Model training & hyperparameter tuning  
- Performance comparison across multiple classifiers  
- Final model selection (Random Forest with GridSearchCV)  
- Preparation for deployment  

## Business Value

- **Early warning system** for banks / financial institutions → reduce non-performing assets (NPAs)  
- **Risk scoring tool** for credit analysts and investment firms  
- **Audit & regulatory support** — identify high-risk entities quickly  
- **Low data requirement** — model uses only 6 ordinal features → feasible even for smaller organizations  
- **High interpretability** — feature importance from tree-based models helps explain predictions  

## Approach & Methodology

1. **Data Understanding & EDA**  
   - Distribution of each feature (bar plots, count plots)  
   - Relationship between features and target (crosstabs, stacked bar charts)  
   - Correlation heatmap & pair plots  

2. **Preprocessing**  
   - No missing values  
   - Features already encoded (0, 0.5, 1) → treated as numerical/ordinal  
   - Train-test split (commonly 80:20 or 70:30)  

3. **Modeling & Evaluation**  
   - Multiple classification algorithms tested  
   - Hyperparameter tuning via GridSearchCV (especially for tree-based models)  
   - Performance metrics: Accuracy, Precision, Recall, F1-score, Confusion Matrix  

4. **Final Model**  
   - **Random Forest Classifier** (after tuning) selected  
   - Achieved perfect / near-perfect performance on the test set (see notebook)  
   - Best parameters identified via grid search  

## Models Compared / Evaluated

(Exact list depends on notebook cells — common ones visible or typically used in such projects:)

- Logistic Regression  
- Decision Tree Classifier  
- Random Forest Classifier (final choice after tuning)  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)  
- Gradient Boosting / XGBoost (if implemented)  

**Final Model Performance** (from notebook – Random Forest after GridSearchCV):  
- Accuracy: **1.00** (100%) on test set  
- Precision / Recall / F1-score: **1.00** for both classes  
- **Note**: Very high performance may indicate small/clean dataset or slight overfitting — cross-validation scores should be reviewed  

## Technologies & Libraries

- **Core**: Python 3, pandas, numpy  
- **Visualization**: matplotlib, seaborn  
- **Modeling**: scikit-learn (RandomForestClassifier, GridSearchCV, metrics)  
- **Warnings handling**: warnings  
- **Planned deployment**: Streamlit / Flask (as per acceptance criterion)

Conclusion
The Random Forest model demonstrates excellent discriminative power on the given dataset, achieving near-perfect classification of bankrupt vs. non-bankrupt companies using only six interpretable risk factors.
This solution can serve as the foundation for a real-world early warning system in banking, credit risk management, and corporate monitoring.


Project Contributors:

Sakshi Parab
Dhanya N
Suyash Dahale
Asad Ansar SK
Rohini Weldode
Yash Shirgaonkar
Niranjan L
