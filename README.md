# Customer Churn Prediction in the Telecommunications Industry

### Created by: Group Beta - Purwadhika Digital School - Data Science Bootcamp Program
**Members:** 
- Zayyan Rafishafa Kabullah Nugraha
- Farry Surachman
- Adi Nugraha

---

## Project Overview

This project focuses on predicting customer churn in the telecommunications industry using the **IBM Telco Customer Churn Dataset**.  
Customer churn. When users stop using a company’s services is a major challenge in telecom. Maintaining customers is much cheaper than acquiring new ones, making churn prediction critical for business success.  

Using machine learning, this project identifies customers who are most likely to leave. This could help the company to act fast before losing their customers.


## Objectives

- Analyze customer demographics, service usage, and billing information.  
- Build and compare machine learning models to predict churn behavior.  
- Identify key factors that influence customer retention.  
- Provide actionable insights to improve customer loyalty.

---

## Dataset Description

The dataset used in this project comes from the **IBM Telco Customer Churn Sample Dataset**.  
Each row represents one customer, and each column contains information about their attributes:

| Category | Description |
|-----------|-------------|
| **Churn** | Indicates whether the customer left in the last month (target variable). |
| **Services** | Type of services used — Phone, Multiple Lines, Internet, Online Security, Backup, Device Protection, Tech Support, Streaming. |
| **Account Info** | Tenure, contract type, payment method, paperless billing, monthly and total charges. |
| **Demographics** | Gender, senior citizen, partner, dependents. |

---

## Machine Learning Workflow

### 1. Data Understanding & Cleaning
- Handle missing values and data inconsistencies.  
- Explore distributions, detect outliers, and visualize relationships between features and churn.  
- Convert categorical variables into numerical format.

### 2. Feature Engineering & Preprocessing
- Encode categorical variables using **OneHotEncoder** or **LabelEncoder**.  
- Scale numerical features using **StandardScaler** or **MinMaxScaler**.  
- Split data into training and testing sets for model validation.

### 3. Modeling
The following models were tested and compared:
- **Logistic Regression**  
- **Decision Tree Classifier**  
- **Random Forest Classifier**  
- **Support Vector Machine (SVM)**  
- **XGBoost / Gradient Boosting**

Performance metrics included:
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- ROC-AUC

### 4. Model Evaluation
- Evaluate model performance on the test set.  
- Use confusion matrix and ROC curve for visual performance assessment.  
- Focus on **recall** to minimize false negatives (important in churn prediction).

### 5. Model Deployment (Optional)
- The final model can be exported as a `.joblib` file and used for real-time prediction (e.g., via Streamlit or Flask app).

## ⚙️ Tools & Libraries

- **Language:** Python 3  
- **Libraries:** pandas, NumPy, scikit-learn, matplotlib, seaborn  
- **Environment:** Google Colab / Jupyter Notebook
- The IBM Telco Customer Churn Dataset can be accessed in https://www.kaggle.com/datasets/blastchar/telco-customer-churn


## How to Run the Notebook

1. Download or clone this repository.  
2. Upload the dataset `WA_Fn-UseC_-Telco-Customer-Churn.csv` to your Colab environment.  
3. Open the notebook `FinalProject_Group_Beta.ipynb` in Google Colab.  
4. Run each cell in sequence.  
5. At the end, a cleaned dataset and trained model file can be exported for further use.

To save the cleaned dataset:
```python
df_cleaned.to_csv('Telco_Customer_Churn_Cleaned.csv', index=False)
