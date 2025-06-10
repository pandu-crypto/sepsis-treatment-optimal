Sepsis Optimal Treatment Plan Using GAN-Based Data Balancing
📌 Project Overview
This project focuses on developing an optimal treatment planning system for sepsis patients using machine learning techniques. The pipeline involves preprocessing a large ICU dataset, balancing highly imbalanced data using GANs, and evaluating multiple ML models to identify the most effective classifier.

🏥 Dataset
Source: ICU patient data (1.5M+ records)

Features: Vitals (HR, O2Sat, SBP, etc.), Admission Info, Demographics

Target: SepsisLabel (binary classification)

🛠️ Preprocessing Steps
Removal of columns with high missing values

Median imputation for missing data

Outlier detection and removal using IQR

Aggregation on Patient_ID for model input

🧪 Model Building
Synthetic Minority Oversampling using GANs

Models trained and evaluated:

Logistic Regression

KNN

SVC

Decision Trees

Random Forest

AdaBoost, GradientBoosting, ExtraTrees

MLP (Neural Net)

Hyperparameter tuning using GridSearchCV

🎯 Performance Metrics
Accuracy, Precision, Recall, F1-Score

Evaluated across both imbalanced and GAN-balanced datasets

Additional breakdowns by patient age group
