 ML Foundations: Census Income Classification Project

**Author**: Angel Espinosa  

## 📌 Project Overview
This project was built as part of the ML Foundations Lab 8 assignment. The goal was to implement a full machine learning pipeline that follows the ML lifecycle from data loading to model evaluation.

## 🧠 Problem Statement
The task is to predict whether an individual earns over \$50K annually using features from the 1994 U.S. Census dataset.

- **Type of Problem**: Supervised binary classification
- **Target Variable**: `income_binary` (<=50K or >50K)

## 📊 Dataset
Dataset used: `censusData.csv`  
Key features used:
- age, workclass, education-num, marital-status, occupation, relationship, race, sex_selfID, capital-gain, capital-loss, hours-per-week, native-country  
- Dropped: `fnlwgt` and `education` (redundant or irrelevant)

## 🔍 Exploratory Data Analysis (EDA)
- Visualized distribution of income classes
- Used boxplots to compare age, hours/week, and education-num against income
- Detected missing values and class imbalance

## ⚙️ Modeling Approach
- Logistic Regression (baseline model)
- Feature encoding: One-hot encoding for categoricals
- Imputation: Median for numericals, mode for categoricals
- Scaled numerical data
- Class weights adjusted for imbalance

## 🔁 Model Tuning
- Hyperparameter tuning via `GridSearchCV`
- 5-fold cross-validation

## 📈 Evaluation Metrics (Final Model)
- **Accuracy**: 81%
- **Precision**: 56.9%
- **Recall**: 85.3%
- **F1 Score**: 68.2%

## ✅ Conclusion
The model successfully identifies individuals likely to earn >\$50K. It can be used by organizations for targeted services, marketing, or financial analysis.

## 📂 Repository Contents
- `census-income-prediction.ipynb`: Jupyter Notebook with full pipeline
- `data/`: Folder containing the dataset (excluded in public repo)
- `README.md`: This file

## Installation & Usage

1. Clone the repo:  
   ```bash
   git clone https://github.com/aespinosa221120/census-income-classification.git
   cd census-income-classification
2. Installed Required Packages
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
3. Run the Jupyter Notebook
   ```bash
   jupyter notebook census-income-prediction.ipynb


## 🙌 Acknowledgments
This project was developed as part of the Fall AID program under the ML Foundations curriculum.
