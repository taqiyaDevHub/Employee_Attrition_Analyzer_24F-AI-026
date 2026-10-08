# Employee Attrition Analyzer

**Name:** Syeda Taqiya Noman  
**Roll No:** 24F-AI-026  
**Lab:** Lab #7 – Open Ended Lab (Machine Learning)

## Overview
A machine learning project that predicts whether an employee is likely to leave a company, using the IBM HR Analytics Employee Attrition & Performance dataset.

## Dataset
IBM HR Analytics Employee Attrition & Performance (`WA_Fn-UseC_-HR-Employee-Attrition.csv`), 1470 employee records with 35 features. Target: `Attrition` (Yes/No).

## Preprocessing
- Checked and filled missing values (none found)
- Dropped constant/ID columns: `EmployeeCount`, `StandardHours`, `Over18`, `EmployeeNumber`
- Encoded `Attrition` as 1/0 and converted categorical columns to numeric using one-hot encoding
- Split data 80/20 (train/test) and applied `StandardScaler`

## Models Used
- Logistic Regression
- Decision Tree (max depth = 5)
- Random Forest

## Results

| Model | F1 Score |
|---|---|
| Logistic Regression | 0.52 |
| Decision Tree | 0.38 |
| Random Forest | 0.25 |

Logistic Regression performed best. The dataset is imbalanced (far more employees stay than leave), so F1 score is more informative than accuracy. Confusion matrices and a feature importance plot (Random Forest) are included in the notebook.

## How to Run
1. Download the dataset from [Kaggle (IBM HR Analytics Employee Attrition & Performance)](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) and place `WA_Fn-UseC_-HR-Employee-Attrition.csv` in the same folder as the notebook
2. Install requirements: `pip install pandas matplotlib seaborn scikit-learn`
3. Open and run `ML_Open_Ended_01.ipynb`
