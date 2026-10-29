# Predictive-Analytics-for-Telecom-Customer-Churn-Using-Machine-Learning

Engineered an end-to-end Python machine learning pipeline to predict telecom customer churn. Designed a robust exploratory data analysis (EDA) and predictive modeling workflow to identify at-risk customers, empowering the business to optimize retention strategies, target marketing efforts, and reduce revenue leakage.

**Project Excerpt**
Architected a data-driven machine learning solution for telecom customer retention. Built a Python-based data processing pipeline, conducted advanced statistical analysis, and deployed optimized classification models to uncover the key demographic and financial drivers of customer attrition.

**Business Case**
Telecommunication companies consistently struggle with high customer turnover, leading to significant revenue loss. Fragmented customer profiles and complex behavioral patterns make it difficult to identify flight risks early. This lack of predictive insight prevents marketing and retention teams from proactively targeting vulnerable customers with customized offers before they cancel their service.

**Project Goal**
To engineer a scalable machine learning pipeline that ingests raw customer demographic and usage data, autonomously cleans anomalies, and feeds optimized classification models to accurately predict the probability of churn and extract actionable business insights.

**Process & Methodology**

*   **Phase 1: Data Preprocessing & Cleaning:** Developed a Pandas-based transformation layer to standardize raw customer records. Programmatically identified and resolved critical data anomalies, specifically addressing missing values in the `TotalCharges` column linked to new customers (`tenure` = 0), ensuring 100% dataset integrity without statistical distortion.
*   **Phase 2: Advanced Exploratory Data Analysis (EDA):** Engineered custom analytical functions and utilized Plotly, Seaborn, and Matplotlib to visualize complex feature distributions. Applied statistical testing (SciPy, Cramer's V) to rigorously quantify correlations between categorical variables (e.g., Contract Type, Internet Service) and churn likelihood.
*   **Phase 3: Pipeline Architecture & Feature Engineering:** Architected automated machine learning pipelines using Scikit-learn. Implemented systematic strategies to handle the highly imbalanced target variable (73.4% retained vs. 26.6% churned) and scaled numerical features to prepare the dataset for algorithmic training.
*   **Phase 4: Predictive Modeling & Hyperparameter Tuning:** Trained, cross-validated, and optimized a suite of classification algorithms including Random Forest, Logistic Regression, Decision Tree, and K-Nearest Neighbors. Utilized `GridSearchCV` to fine-tune model parameters, evaluating performance across Accuracy, Precision, Recall, and F1-Score metrics to select the most robust predictor.

**Key Insights & Analytical Wins**

*   **Contract Type Vulnerability:** Uncovered that contract length is the single strongest predictor of churn. Analysis revealed a staggering 75% churn rate among customers on Month-to-Month contracts, compared to just 13% for one-year and a minimal 3% for two-year contracts.
*   **Service-Specific Risk Isolation:** Identified a critical retention vulnerability within the "Fiber optic" internet service tier, which exhibited an unexpectedly high churn rate compared to DSL, signaling a need for immediate service quality review or targeted pricing interventions.
*   **Demographic Drivers:** Discovered that Senior Citizens and customers without partners or dependents are significantly more likely to churn, whereas gender was statistically proven to have zero impact on a customer's decision to leave.

**Impact**

*   **Targeted Retention Strategy:** Provided highly actionable customer segmentation metrics, allowing business stakeholders to shift from reactive customer service to proactive, data-driven retention campaigns (e.g., incentivizing Month-to-Month users to upgrade to annual contracts).
*   **Optimized Analytical Pipeline:** Delivered a reusable, scalable Python foundation primed for continuous data ingestion, drastically reducing the time required to process new customer batches and generate updated churn probability scores.
*   **Data Integrity & Reliability:** Eradicated logical data conflicts and missing value anomalies early in the ETL process, ensuring that the downstream machine learning models were trained on pristine, mathematically sound data.

**Tools & Technologies Used**

*   **Data Engineering & Analysis:** Python (Pandas, NumPy, SciPy)
*   **Machine Learning:** Scikit-learn (Pipelines, GridSearchCV, RandomForest, LogisticRegression, DecisionTree, KNeighbors)
*   **Data Visualization:** Plotly, Seaborn, Matplotlib

**Data Sources & Overview**

*   **Data Origin:** Telco Customer Churn Dataset (7,043 customer records)
*   **Features:** 
    *   **Demographics:** Gender, SeniorCitizen, Partner, Dependents.
    *   **Services:** PhoneService, MultipleLines, InternetService, and add-ons (OnlineSecurity, TechSupport, Streaming).
    *   **Account Information:** Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges, Tenure.
    *   **Target Variable:** `Churn` (Yes/No indicating whether the customer left the company).
*   **Note:** The initial exploratory analysis and data cleaning were isolated to ensure pristine feature engineering before the dataset was passed into the separate machine learning modeling and evaluation workflow.

**Team Members**
*   Hazem Mohamed Samy – hazemmuhammedd1@gmail.com
*   Mahmoud Emam Elhout – ma7moudel7out@gmail.com
*   Tarek Ahmed Ali – Tareahme@gmail.com
*   Asmaa Gamal AbdElnasser – gasmaa188@outlook.com