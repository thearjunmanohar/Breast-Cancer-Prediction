# Breast Cancer Prediction using Machine Learning

## 📌 Project Overview

Breast cancer is one of the most common and life-threatening diseases among women worldwide. Early and accurate detection plays a critical role in improving survival rates.

This project focuses on building an **end-to-end machine learning classification system** to predict whether a tumor is **Malignant (cancerous)** or **Benign (non-cancerous)** using diagnostic features. The project covers the complete ML workflow, from data understanding to model evaluation and comparison.

---

## 🎯 Problem Statement

Build a supervised machine learning model that can accurately classify breast tumors as *Malignant* or *Benign* based on diagnostic measurements.

---

## 📊 Dataset Information

* **Dataset**: Breast Cancer Wisconsin (Diagnostic)
* **Target Variable**: `diagnosis`

  * `M` → Malignant
  * `B` → Benign
* **Features**: Numerical features describing tumor characteristics such as radius, texture, smoothness, concavity, symmetry, etc.

This is a **binary classification problem**, as the output consists of discrete class labels.

---

## 🔍 Exploratory Data Analysis (EDA)

The following checks were performed to understand the dataset:

* Dataset shape and structure
* Data types of all features
* Missing value analysis
* Duplicate row detection
* Statistical summary of numerical features
* Target class distribution

### ⚠️ Class Imbalance

The dataset exhibits an imbalance between *Benign* and *Malignant* cases. Since false negatives are critical in medical applications, addressing class imbalance is an important step.

---

## 🛠️ Data Preprocessing

### Feature–Target Separation

* **X (Features)**: All diagnostic measurements
* **y (Target)**: Tumor diagnosis

### Handling Class Imbalance

* **Undersampling** was applied to balance the dataset
* Chosen for learning simplicity and to reduce bias toward the majority class

> Note: Advanced approaches such as **SMOTE** or **class_weight adjustment** can be explored for production-grade systems.

### Train–Test Split

* The dataset was split into training and testing sets
* Ensures unbiased evaluation of model performance

### Feature Scaling

* **StandardScaler** was used for feature scaling
* Essential for distance-based algorithms like KNN
* Scaler was fitted only on training data to prevent data leakage

---

## 🤖 Model Building

Multiple classification models were trained and compared:

### K-Nearest Neighbors (KNN)

* Distance-based classification algorithm
* Highly sensitive to feature scaling
* Works well with clearly separated class boundaries

### Naive Bayes

* Probabilistic classifier based on Bayes’ Theorem
* Assumes feature independence
* Performs efficiently on high-dimensional data

### Decision Tree (Entropy / ID3)

* Tree-based model using information gain for splits
* Captures non-linear relationships
* Offers interpretability through decision rules

---

## 📈 Model Evaluation

Given the medical context, **recall** is prioritized over accuracy, as misclassifying a malignant tumor as benign can have severe consequences.

### Evaluation Metrics Used

* Confusion Matrix
* Accuracy
* Precision
* Recall
* F1-Score

Each model was evaluated on the test dataset using these metrics.

---

## 🔎 Model Comparison

* Classification reports were used to compare all models
* Special focus on **recall for the Malignant class**
* The model with the best balance between recall and overall performance was considered the most suitable

---

## 📘 Key Takeaways

* Importance of handling class imbalance in medical datasets
* Why evaluation metrics must align with domain objectives
* Impact of feature scaling on distance-based models
* Trade-offs between interpretability and predictive performance

---

## ✅ Conclusion

This project demonstrates a complete **end-to-end machine learning workflow**, from raw data exploration to model evaluation and comparison. While the current implementation is suitable for learning and experimentation, it provides a strong foundation for more advanced, production-ready systems.

The project highlights solid fundamentals in **data preprocessing, model selection, and evaluation strategy**, making it suitable for ML portfolios and entry-level interviews.

---

## 🚀 Future Improvements

* Hyperparameter tuning using `GridSearchCV`
* SMOTE for improved class imbalance handling
* Feature importance and interpretability analysis
* Pipeline creation for production readiness
* Model deployment using Flask or FastAPI

---

## ▶️ How to Run the Project

1. Clone the repository
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook:

   ```bash
   jupyter notebook
   ```
