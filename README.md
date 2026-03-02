# Cloud-Based Credit Card Fraud Detection Pipeline

## 🚀 Overview
An end-to-end Machine Learning pipeline utilizing **Snowflake** for cloud data warehousing and **Scikit-Learn** for predictive modeling. This project implements a high-performance Random Forest classifier to detect fraudulent transactions with a focus on high recall and cloud scalability.

## 🏗️ Architecture (Medallion Flow)
- **Bronze/Raw**: Initial transaction ingestion into Snowflake.
- **Silver/STG**: Data cleaning and feature engineering using **RobustScaler** to mitigate the impact of extreme outliers.
- **Gold**: Final model predictions and performance metrics persisted back to Snowflake for business intelligence.

## 🧪 Mathematical Foundation
- **Robust Scaling**: Utilized the Interquartile Range (IQR) to scale features, ensuring the 30-dimensional vector space remained robust against fraudulent outliers.
- **Dimensional Separability**: Leveraged PCA-transformed features (V1-V28) to identify high-variance axes critical for classification.
- **Class Imbalance**: Applied Under-sampling to the majority class to achieve a balanced training environment.

## 📊 Results
- **Recall (Fraud Class)**: **0.90** (Caught 90% of all fraudulent attempts).
- **Precision**: **1.00** (Zero false positives recorded).
- **Overall Accuracy**: **94%**.

## 🛠️ Tech Stack
- **Languages**: Python (Pandas, NumPy, Matplotlib)
- **Database**: Snowflake (Snowpark API)
- **ML Library**: Scikit-Learn (Random Forest Classifier)
- **DevOps**: Git/GitHub for Version Control
