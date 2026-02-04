# Heart-Disease-Prediction-Full-Pipeline-
End-to-end machine learning pipeline for heart disease prediction using real-world medical data, with proper preprocessing, class imbalance handling, and model comparison.
# ❤️ Heart Disease Prediction  
## End-to-End Machine Learning Pipeline

## 📌 Project Motivation
Heart disease is one of the leading causes of death worldwide.  
The objective of this project is to build a **machine learning pipeline** that can predict the presence of heart disease using patient clinical data, while following **real-world data science practices**.

This project focuses not only on model accuracy, but on:
- Understanding the data
- Handling real medical data problems
- Building clean and reusable pipelines
- Evaluating models fairly

---

## 📊 Dataset Summary
- **Domain:** Healthcare / Medical
- **Problem Type:** Binary Classification
- **Target Variable:** Heart Disease (0 = No, 1 = Yes)
- **Features:**  
  - Numerical features (e.g. age, cholesterol, blood pressure)
  - Categorical features (e.g. sex, chest pain type)

The dataset represents **real clinical data**, which makes it imperfect and challenging — similar to what is encountered in real projects.

---

## ❗ Problem Definition
The core problem is to:
> Predict whether a patient has heart disease based on clinical measurements.

However, the real challenge was not the model itself, but:
- Missing values
- Mixed feature types
- Class imbalance
- Avoiding data leakage during preprocessing

---

## 🔍 Data Understanding & Challenges

### 1️⃣ Missing Values
- Many features contained missing values.
- Both numerical and categorical columns were affected.
- Dropping rows was not an option due to data loss risk.

➡️ **Solution:**  
We used appropriate imputation strategies for numerical and categorical features inside a pipeline.

---

### 2️⃣ Mixed Data Types
- The dataset includes numerical and categorical variables.
- Each type requires different preprocessing techniques.

➡️ **Solution:**  
We built separate preprocessing pipelines and combined them using a `ColumnTransformer`.

---

### 3️⃣ Class Imbalance
- The target variable was imbalanced.
- Models trained without handling imbalance tend to favor the majority class.

➡️ **Solution:**  
We applied **SMOTE** to oversample the minority class inside the training pipeline.

---

## 🔍 Exploratory Data Analysis (EDA)
EDA was performed to better understand the data:
- Missing value distribution was analyzed
- Target class distribution was examined
- Feature relationships with the target were explored

This step helped guide preprocessing choices and model evaluation strategy.

---

## 🧹 Data Preprocessing Pipeline

A clean and modular preprocessing pipeline was implemented:

### Numerical Features
- Missing values handled using statistical imputation
- Standard scaling applied

### Categorical Features
- Missing values handled separately
- One-hot encoding applied

### Unified Pipeline
- Combined numerical and categorical pipelines
- Ensured consistent preprocessing across all models
- Prevented data leakage

---

## ✂️ Train-Test Split
- Data was split into training and testing sets
- Preprocessing was applied **after** splitting
- This ensured fair evaluation on unseen data

---

## ⚖️ Handling Class Imbalance
- SMOTE was applied only on the training data
- Integrated into an `imblearn` pipeline
- Prevented target leakage and overfitting

---

## 🤖 Models Trained
Multiple machine learning models were implemented and compared:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost

All models used the **same preprocessing and resampling pipeline**, ensuring a fair comparison.

---

## 📈 Model Evaluation
Models were evaluated using:
- Accuracy
- Recall
- F1-score
- Confusion Matrix

Special attention was given to **recall**, as detecting heart disease cases is more critical than overall accuracy.

---

## 🏆 Model Comparison & Selection
- Model performances were visualized using comparison plots
- XGBoost achieved the best overall performance
- It showed stronger detection of heart disease cases and better generalization

---

## ✅ What We Learned (Key Takeaways)
From this project, we learned that:
- Real medical data is noisy and incomplete
- Proper preprocessing is as important as model selection
- Class imbalance can seriously mislead performance metrics
- Pipelines are essential for clean, reusable, and safe ML workflows
- Ensemble models can significantly improve results when combined with proper data handling

---

## 🚀 Project Value
This project demonstrates:
- End-to-end machine learning thinking
- Strong data preprocessing skills
- Ability to handle real-world healthcare data
- Production-ready pipeline design

It is suitable for **Data Scientist and Machine Learning Engineer portfolios**.

---

## 📂 Repository Structure

