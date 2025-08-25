# 🍷 Beverage Quality Classification using Logistic Regression

This project aims to predict the **quality of beverages (wine)** based on physicochemical test results using **machine learning techniques**. By cleaning the data, analyzing correlations, and building logistic regression models, we evaluate the ability to classify quality into **Poor**, **Normal**, and **Excellent**.

---

## 🎯 Project Objective

To develop a supervised machine learning model that classifies beverages into **three quality categories** based on physicochemical properties like acidity, sugar content, alcohol level, pH, etc.

---

## 📂 Dataset Overview

- **Source:** Beverage dataset (similar to Wine Quality)
- **Size:** 3961 unique records
- **Features:**
  - `fixed acidity`
  - `volatile acidity`
  - `citric acid`
  - `residual sugar`
  - `chlorides`
  - `free sulfur dioxide`
  - `total sulfur dioxide`
  - `density`
  - `pH`
  - `sulphates`
  - `alcohol`
  - `quality` (Target: Poor, Normal, Excellent)

---

## 🧹 Data Preprocessing

1. **Missing Values:** No null values detected.
2. **Duplicates:** 937 duplicate records dropped.
3. **Target Encoding:**  
   - 'Poor' → 0  
   - 'Normal' → 1  
   - 'Excellent' → 2  
4. **Feature Correlation:** Selected relevant features based on correlation thresholds:
   - `cor_1`: features with correlation > 0.05
   - `cor_2`: features with correlation > 0.1

---

## 📊 Class Distribution (after encoding)

| Class      | Count |
|------------|-------|
| Normal (1) | 2963  |
| Excellent (2) | 825  |
| Poor (0)   | 173   |

---

## 📌 Feature Selection

Two feature subsets were created based on correlation thresholds:
- **Subset 1 (cor > 0.05):** 8 features
- **Subset 2 (cor > 0.1):** 7 features

---

## ⚙️ Model Building

- **Model Used:** Logistic Regression
- **Train/Test Split:** 80% training, 20% testing
- **Evaluation Metrics:**
  - Confusion Matrix
  - Classification Report (Precision, Recall, F1-Score)

---

## 📈 Results

### 🔹 Model on Feature Subset 1 (cor > 0.05)

- **Accuracy:** 78%
- **Observations:**
  - Strong performance on Normal class
  - Poor recall for Poor and Excellent categories
  - Model struggled with class imbalance

### 🔹 Model on Feature Subset 2 (cor > 0.1)

- **Accuracy:** 77%
- **Observations:**
  - Similar trends as above
  - Better precision on Excellent class but very low recall for Poor

---

## 🧠 Key Insights

- **Alcohol level** shows the highest positive correlation with quality.
- **Density** and **total sulfur dioxide** show strong negative correlations.
- Logistic Regression performs well on dominant class but struggles on underrepresented ones (class imbalance).
- Better performance could be achieved with:
  - Data balancing (SMOTE, oversampling)
  - Scaling features
  - Using tree-based models (Random Forest, XGBoost)

---

## 📌 Future Work

- Implement advanced models (Random Forest, XGBoost, Neural Networks)
- Apply SMOTE or class weighting to handle imbalance
- Hyperparameter tuning (increase `max_iter`, change solver)
- Feature scaling and normalization
- Build an interactive Streamlit dashboard

---

## 📊 Technologies Used

- **Language:** Python
- **Libraries:**  
  - Pandas, NumPy, Matplotlib  
  - Scikit-learn (Logistic Regression, Train-Test Split, Evaluation Metrics)  

---

## 👨‍💻 Author

**Nisarga Shivamurthy Maheshwarappa**  
📧 [nisargasm2@gmail.com](mailto:nisargasm2@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/nisarga-s-m)

---

