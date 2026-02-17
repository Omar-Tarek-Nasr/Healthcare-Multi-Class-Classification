# Healthcare Multi-Class Classification
<img width="1024" height="554" alt="img" src="https://github.com/user-attachments/assets/d61ae36d-a6f5-4593-99b5-0bdb3ab7a97e" />

## 🏥 Signal or Noise?  

### 📌 Project Overview

This project investigates a fundamental Machine Learning question:

> What happens when you train models on a clean, well-structured dataset — but the data lacks meaningful predictive signal?

This was my **second project during my internship at Uneeq Interns**, where I explored a healthcare multi-class classification problem aiming to predict medical test results.

---

## 🎯 Problem Statement

The goal was to predict the outcome of medical test results based on patient information.

### Target Classes:
- Normal  
- Abnormal  
- Inconclusive  

This is a **multi-class classification problem**.

---

## 📊 Dataset Description

The dataset includes structured healthcare-related information such as:

- Age  
- Gender  
- Medical Condition  
- Insurance Provider  
- Admission Type (Emergency, Urgent, Routine)  
- Medications  
- Date of Admission  
- Discharge Date  
- Doctor & Hospital information  

### Data Quality:
- No missing values  
- No duplicates  
- Balanced target classes  
- Clean categorical and numerical structure  

At first glance, the dataset appeared ideal for modeling.

---

## 🧠 Feature Engineering

To enhance predictive potential:

- Calculated **length of hospital stay** using:


- Removed high-cardinality features (e.g., patient names, doctor names, hospital names, room numbers)
- Prepared categorical and numerical features separately

---

## 🔍 Exploratory Data Analysis (EDA)

Performed:

- Distribution analysis of numerical features  
- Count plots for categorical variables  
- Class balance verification  
- Outlier checks  
- General statistical summaries  

Findings:
- Data distributions were reasonable  
- No extreme imbalance  
- No obvious anomalies  

---

## ⚙️ Preprocessing Pipeline

Used a structured and professional ML workflow:

- Stratified train/test split  
- One-Hot Encoding for categorical variables  
- Standard Scaling for numerical variables  
- ColumnTransformer for feature separation  
- Pipeline to prevent data leakage  

---

## 🤖 Models Used

- Logistic Regression  
- Random Forest Classifier  

Both models were evaluated using:

- Accuracy  
- Cross-validation  
- Feature importance  
- Mutual Information  

---

## 🚨 Results

- Accuracy ≈ 33%  
- Performance equivalent to random guessing  
- Cross-validation confirmed stable but weak results  
- No strong feature importance detected  
- Mutual Information scores were extremely low  

---

## 🔎 Root Cause Analysis

After thorough evaluation, the conclusion was clear:

> The dataset lacked meaningful predictive signal connecting input features to the target variable.

The issue was not:
- Overfitting  
- Underfitting  
- Model selection  
- Preprocessing errors  

The issue was the absence of informative relationships in the data itself.

---

## 💡 Key Learnings

- Not every clean dataset is predictive.  
- Model performance depends on signal, not cleanliness.  
- Feature-target relationships must be validated early.  
- Cross-validation is essential for confirming consistency.  
- Mutual Information helps detect weak predictive power.  

This project reinforced a critical Machine Learning mindset:

> Before optimizing the model, validate whether the data can actually answer the question.

---

## 🚀 Suggested Future Improvements

- Apply advanced feature selection techniques  
- Try boosting models (XGBoost / LightGBM)  
- Investigate domain-specific feature enrichment  
- Explore binary reformulation of the problem  
- Apply SHAP analysis for deeper interpretability  

---

## 🏷 Suggested Project Name Options

- **Signal or Noise: Healthcare Classification Study**
- **When Clean Data Fails**
- **Predictive Signal Validation in Healthcare Data**
- **Understanding Feature-Target Weakness in ML**
- **Healthcare ML: A Study in Signal Detection**

---

## 📌 Conclusion

This project was less about achieving high accuracy  
and more about understanding the limits of data.

It represents an important step in developing a mature Machine Learning mindset —  
focusing not just on models, but on validating signal strength and data relevance.

---


## 🔬 Key Findings & Model Insights

####  Data Analysis & Distribution
* **Balanced Classes:** The dataset exhibits a **balanced class distribution**, ensuring that the models were not biased toward a specific category.
* **Statistical Significance:** Initial statistical tests suggest a **weak association** between the selected features and the target variable, indicating a lack of strong predictive signals.

---

####  Model Performance Summary
Despite experimenting with different algorithms, the predictive power remained limited:

| Model | Performance (Accuracy) | Status |
| :--- | :--- | :--- |
| **Logistic Regression** | ~33% | Random Baseline |
| **Random Forest** | ~33% | Random Baseline |

> **Note:** In a balanced 3-class problem, an accuracy of **~33%** is equivalent to a **random guess**.

---

####  Reliability & Validation
* **Consistent Results:** Automated **Cross-Validation** confirmed that the low performance is stable across different data folds, ruling out issues with specific data splits.
* **Feature Importance:** Analysis revealed **no dominant predictors**; no single feature contributed significantly to the model's ability to distinguish between classes.

---

####  Technical Conclusion
The models are currently unable to capture a meaningful pattern from the provided features. This suggests that the **underlying signal is either missing** from the current dataset or the relationship is too complex for the current feature set to represent.
