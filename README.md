# Diabetes Risk Classification

A machine learning project that predicts diabetes risk using demographic, behavioral, and health-related indicators collected from the CDC Behavioral Risk Factor Surveillance System (BRFSS).

This project develops and compares multiple supervised learning models to identify individuals at high risk of diabetes and to uncover the most influential health factors contributing to disease risk. The results provide data-driven insights that can support preventive healthcare strategies and public health decision-making.

---

## Project Overview

Diabetes is one of the most common chronic diseases worldwide and continues to place a significant burden on healthcare systems. Early identification of high-risk individuals allows healthcare providers to implement preventive interventions before severe complications develop.

This project builds a binary classification model using health indicator data to predict diabetes risk and identify the lifestyle and demographic factors that contribute most to disease development.

---

## Business Problem

Healthcare organizations and policymakers need effective methods to identify populations at elevated risk for diabetes so that prevention resources can be allocated more efficiently.

The primary business question addressed in this project is:

> How can lifestyle and behavioral factors be prioritized to reduce diabetes risk across different demographic groups?

The resulting model can support early risk screening, targeted health education, and evidence-based public health initiatives.

---

## Dataset

**Dataset**

Diabetes Health Indicators Dataset (BRFSS 2015)

File included in this repository:

```
diabetes_binary_health_indicators_BRFSS2015.csv
```

Dataset characteristics:

- 253,680 observations
- Binary diabetes outcome
- 21 health-related features

Features include:

- BMI
- Age
- High Blood Pressure
- High Cholesterol
- Smoking
- Physical Activity
- General Health
- Income
- Education
- Physical Health
- Mental Health

The dataset originates from the CDC Behavioral Risk Factor Surveillance System (BRFSS 2015). :contentReference[oaicite:0]{index=0}

---

## Project Workflow

1. Data exploration
2. Data preprocessing
3. Feature engineering
4. Feature selection
5. Model training
6. Hyperparameter tuning
7. Model evaluation
8. Feature interpretation
9. Business recommendations

---

## Data Preprocessing

Several preprocessing techniques were applied before model training:

- Missing value handling
- Feature scaling using StandardScaler
- Class imbalance handling using class weights
- Train-test split
- Feature importance analysis

The dataset contained approximately:

- 85% non-diabetic individuals
- 15% diabetic individuals

making class imbalance an important consideration during model development. :contentReference[oaicite:1]{index=1}

---

## Machine Learning Models

The following supervised learning algorithms were evaluated:

- Logistic Regression
- Decision Tree
- Random Forest
- Balanced Random Forest
- Gradient Boosting Trees
- XGBoost

Hyperparameters were optimized using GridSearchCV and RandomizedSearchCV before comparing model performance. :contentReference[oaicite:2]{index=2}

---

## Model Evaluation

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC AUC

Because healthcare applications prioritize minimizing false negatives, Recall and ROC AUC were considered the most important evaluation metrics during model selection. :contentReference[oaicite:3]{index=3}

---

## Final Model

The final deployed model is a **Gradient Boosting Classifier** with class weighting.

Reasons for selection:

- Highest ROC AUC (0.826)
- Strong balance between Recall and Precision
- Good generalization performance
- Effective handling of nonlinear feature interactions

Compared with the other evaluated models, Gradient Boosting achieved the best overall predictive performance while maintaining robust classification of high-risk individuals. :contentReference[oaicite:4]{index=4}

---

## Feature Importance

Feature importance analysis and SHAP values identified the following variables as the strongest predictors of diabetes risk:

- General Health
- High Blood Pressure
- BMI
- Age
- High Cholesterol

These features consistently contributed the most to model predictions across multiple evaluation methods. :contentReference[oaicite:5]{index=5}

---

## Key Findings

The analysis suggests several important health indicators associated with elevated diabetes risk:

- Higher BMI substantially increases diabetes risk.
- High blood pressure becomes increasingly important with age.
- High cholesterol consistently contributes to elevated diabetes risk.
- Poor general health strongly predicts diabetes.
- Mobility limitations are associated with higher disease probability.

Interaction analyses further demonstrate that diabetes risk is influenced by combinations of health conditions rather than isolated factors. :contentReference[oaicite:6]{index=6}

---

## Business Recommendations

Based on the model results, healthcare organizations should prioritize:

- Weight management programs for high-BMI individuals
- Blood pressure monitoring for adults over 40
- Cholesterol screening and preventive care
- Routine health assessments for high-risk populations
- Smoking cessation and physical activity initiatives

These interventions can improve early detection and reduce long-term healthcare costs through targeted prevention strategies. :contentReference[oaicite:7]{index=7}

---

## Repository Structure

```
diabetes-risk-classification/

│
├── Code.ipynb
├── Diabetes Risk Prediction Report.pdf
├── Diabetes Risk Prediction Presentation.pdf
├── diabetes_binary_health_indicators_BRFSS2015.csv
└── README.md
```

---

## Repository Contents

| File | Description |
|------|-------------|
| Code.ipynb | Data preprocessing, feature engineering, model training, and evaluation |
| Diabetes Risk Prediction Report.pdf | Complete project report with methodology and findings |
| Diabetes Risk Prediction Presentation.pdf | Project presentation summarizing key results |
| diabetes_binary_health_indicators_BRFSS2015.csv | Diabetes Health Indicators dataset |
| README.md | Project documentation |

---

## Future Improvements

Potential future work includes:

- Incorporating longitudinal patient records
- Applying deep learning models
- Improving model fairness across demographic groups
- Developing a web-based diabetes risk assessment tool
- Deploying the model through a REST API for clinical use

---

## Team

Master of Business Analytics

UBC Sauder School of Business

- Sisly Lyu
- Diana Lee
- Xiaoxi Xu
- Julia Krumgant
- Nick Shao

---

## Skills Demonstrated

- Machine Learning
- Binary Classification
- Python
- Scikit-learn
- Data Preprocessing
- Feature Engineering
- Hyperparameter Tuning
- Model Evaluation
- Gradient Boosting
- Random Forest
- XGBoost
- SHAP
- Feature Importance
- Healthcare Analytics
