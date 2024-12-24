# Credit Scoring Model for Loan Default Prediction

## Project Overview
This project develops a credit scoring model for "Prêt à Dépenser," a consumer credit company. The goal is to predict the probability of loan default for clients with limited credit history. The project incorporates data preprocessing, machine learning, and advanced interpretability techniques to ensure transparency and improve decision-making in loan approvals.

## Objectives
- **Data Exploration**:
  - Analyze a dataset of 307,000 clients with 121 features.
  - Handle class imbalance in the target variable (`TARGET`).
- **Model Development**:
  - Train and evaluate classification models (Logistic Regression, Random Forest, XGBoost, LightGBM).
  - Optimize hyperparameters using grid search with AUC-ROC as the key metric.
- **Interpretability**:
  - Use SHAP (SHapley Additive ExPlanations) for global and local feature importance.
  - Provide transparency in credit decision-making.

## Tools & Techniques
- **Data Preprocessing**:
  - Encoded categorical variables using Label Encoding and One-Hot Encoding.
  - Addressed missing values with imputation techniques.
  - Balanced target classes using SMOTE and undersampling.
- **Modeling**:
  - Evaluated models: Dummy Classifier, Logistic Regression, Random Forest, XGBoost, LightGBM.
  - LightGBM selected as the best model based on AUC-ROC and F2 scores.
- **Monitoring**:
  - Used Evidently AI to detect data drift in 10 key columns, including `TARGET`.
  - Recommended proactive model updates to adapt to changing data distributions.
- **Evaluation Metrics**:
  - AUC (Area Under the Curve)
  - F2 Score
  - Recall
  - Precision

## Key Results
- **Best Model**: LightGBM achieved the highest AUC-ROC and balanced performance across metrics.
- **Feature Importance**:
  - External sources of credit scores (EXT_SOURCE_1, EXT_SOURCE_2, EXT_SOURCE_3) were most influential.
  - Loan amount (`AMT_CREDIT`) and client age (`DAYS_BIRTH`) also played significant roles.
- **Interpretability**:
  - SHAP values provided actionable insights for client-level predictions.

## Deliverables
- **Jupyter Notebooks**:
  - Exploratory Data Analysis (EDA) and Feature Engineering.
  - Model training, evaluation, and interpretability analysis.
- **Presentation**:
  - Summarized methodology, results, and future improvements.
- **Documentation**:
  - Detailed methodological note for transparency.

## Future Work
- Explore additional feature engineering using external data sources.
- Automate model retraining to handle data drift.
- Integrate client feedback to refine predictions.
