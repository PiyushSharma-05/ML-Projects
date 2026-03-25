<h1 align="center">💳 CreditWise: Loan Approval Prediction System</h1>
<p align="center"><i>A Machine Learning approach to automated credit risk assessment.</i></p>

<br>
An end-to-end Machine Learning pipeline designed to automate and predict loan eligibility using historical applicant data. This project explores the trade-offs between precision and recall in a financial risk context.


<br>
<br>

🚀 Overview
<br>

Dataset: 1,000 entries with 20 features (Income, Credit Score, DTI Ratio, etc.)

Goal: Binary classification of Loan_Approved (Yes/No).

Key Challenge: Handling missing data (5% per column) and optimizing for risk-sensitive metrics.

<br>

🛠️ Technical Workflow
<br>

1. Data Preprocessing & EDA

Imputation: Used SimpleImputer with mean for numerical and most_frequent for categorical missing values.

Visualization: Detailed analysis using Seaborn (Heatmaps, Boxplots, and Pie charts) to identify correlations between Credit_Score, DTI_Ratio, and approval rates.

Encoding: Implemented LabelEncoder for ordinal data and OneHotEncoder (drop='first') for nominal features.

<br>

2. Feature Engineering
<br>

Non-linear Transformations: Created polynomial features (DTI_Ratio_sq, Credit_Score_sq) to capture complex relationships.

Scaling: Applied StandardScaler to ensure distance-based models (KNN) and gradient-based models (Logistic Regression) perform optimally.

<br>

3. 📊 Model Performance Comparison
 <br>

I compared three distinct algorithms to evaluate the "Precision vs. Recall" trade-off:


| Model | Accuracy | Precision | Recall | F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| **Logistic Regression** | 88% | 0.79 | 0.80 | 0.80 |
| **Gaussian Naive Bayes** | 86% | 0.78 | 0.77 | 0.78 |
| **K-Nearest Neighbors** | 76% | 0.62 | 0.51 | 0.56 |

<br>

📈 Key Insight
<br>

Logistic Regression emerged as the superior model for this dataset, achieving a balanced F1-score of 0.80. While Gaussian NB remained competitive, the engineered features helped Logistic Regression better distinguish between high-risk and low-risk applicants.

<br>

📂 Project Structure
<br>

loan_system.ipynb: Cleaned and documented Jupyter Notebook.


loan_data.csv: Raw dataset.


model_comparison.png: Visual performance summary.
