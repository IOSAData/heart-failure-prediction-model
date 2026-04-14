# Predictive Cardiology: Heart Failure Mortality Prediction

## Project Overview
This project bridges clinical pathology and data science by building a machine learning pipeline capable of predicting patient mortality risk. Utilizing the standard Heart Failure Clinical Records dataset, this project processes 13 clinical features (including ejection fraction, serum creatinine, and blood pressure) to evaluate and predict survival outcomes.

## The Core Problem
In clinical cardiology, assessing heart failure risk relies on evaluating a complex matrix of vitals and biomarkers. The goal of this project is to automate and enhance this triage process by training algorithms to detect high-risk patterns in patient data that might otherwise go unnoticed.

## Technology Stack
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (Logistic Regression, Random Forest Classifier)
* **Data Scaling:** StandardScaler
* **Environment:** Google Colab

## Methodology & Pipeline
1. **Exploratory Data Analysis (Clinical Triage):** Conducted a preliminary review of the dataset to verify patient volume, check for missing values, and analyze the statistical spread of the vitals.
2. **Data Standardization:** Machine learning models require balanced numerical inputs. Applied `StandardScaler` to ensure vitals with naturally larger numerical ranges (like platelet count) did not artificially overpower smaller-scale vitals (like serum creatinine).
3. **Algorithm Initialization:** Deployed two distinct models to compare diagnostic approaches:
   * **Logistic Regression (The Clinical Risk Score):** Assigns mathematical weights to specific vitals, functioning similarly to a standard clinical risk scoring system (e.g., CHADS₂).
   * **Random Forest Classifier (The Multidisciplinary Team):** An ensemble model utilizing 100 decision trees to evaluate complex, overlapping patient features and generate a consensus diagnosis.
4. **Evaluation:** Tested both models on a 20% unseen patient subset, evaluating not just raw accuracy, but specific clinical metrics including Precision (minimizing false positives) and Recall/Sensitivity (minimizing false negatives).

## Real-World Application
This pipeline demonstrates how predictive analytics can be integrated into electronic health records (EHR). By instantly flagging high-risk patients based on real-time lab results, these models can act as a "digital triage nurse," allowing attending physicians to allocate resources to critical patients faster and more efficiently.
