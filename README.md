# 🩺 Breast Cancer Classification using SVM  
**Predicting malignancy with precision. From data to diagnosis.**  

---

## 📚 Project Overview

This machine learning project tackles binary classification on the **Breast Cancer Wisconsin (Diagnostic)** dataset using **Support Vector Machines (SVM)**. The objective is to accurately classify tumors as **malignant (M)** or **benign (B)** using both **linear** and **RBF kernels**, with a focus on performance tuning and visualization.

> ✅ Key steps: Data cleaning, feature scaling, training SVM models, PCA-based visualization, hyperparameter tuning, and performance evaluation.

---

## 🗃️ Dataset Summary

- **File used**: `Breast_cancer.csv`
- **Total Samples**: 569
- **Features**: 30 numerical features (mean, error, worst)
- **Target Variable**: `diagnosis`  
  - `M` → 1 (Malignant)  
  - `B` → 0 (Benign)
- **Missing Values**: None ❌

---

## 🧹 Data Preparation

- Dropped non-contributory columns (`id`, unnamed).
- Encoded the target column (`diagnosis`).
- Standardized features using **StandardScaler** to balance feature importance.
- Dataset split into **70% training** and **30% testing**.

---

## 🧠 Modeling Pipeline

### 🔹 SVM with Linear Kernel
- Trained as a baseline.
- Captured linearly separable trends in data.

### 🔹 SVM with RBF Kernel
- Implemented to detect non-linear boundaries.
- Outperformed linear in flexibility.

### 🔧 Hyperparameter Tuning
- Used **GridSearchCV** with 5-fold CV to explore optimal:
  - `C`: [0.1, 1, 10]
  - `gamma`: [1, 0.1, 0.01]
- Best parameters selected for RBF kernel post tuning.

---

## 📊 Accuracy Results

| Model                        | Accuracy      |
|-----------------------------|---------------|
| SVM (Linear)                | 97.66%        |
| SVM (RBF)                   | 97.66%        |
| Tuned SVM (RBF)             | 95.32%        |
| Retrained SVM (Post-Tuning) | **96.49%**    |

🌀 **Cross-validation** was used during tuning to ensure model generalization and robustness.

---

## 📉 Visualization (PCA)

- Reduced feature dimensions using **Principal Component Analysis (PCA)** to 2D.
- Visualized:
  - Class separation in PCA space.
  - Decision boundaries of the best-performing model.
- Observed distinct clusters for malignant and benign tumors — aiding interpretability.

---

## 🛠️ Tools & Libraries

- `pandas`, `numpy` – Data manipulation
- `matplotlib`, `seaborn` – Visual storytelling 📊
- `scikit-learn` – ML modeling, PCA, tuning

---

## 💡 Learnings

- 📈 Even small improvements in medical ML can be life-changing.
- 🔍 RBF kernel SVM can flexibly adapt to non-linear patterns.
- 🔧 Tuning is a tradeoff: performance vs generalization.
- 🎯 Accuracy is high, but visual tools like PCA help bridge the interpretability gap.

---

## 💬 How to Run

1. Upload `Breast_cancer.csv` in a Colab or Jupyter environment.
2. Follow the notebook step-by-step.
3. Optional: Modify kernel types or parameters to explore!

---

## ❤️ About This Project

This project blends precision engineering with medical data science. Through streamlined pipelines, it highlights how **Support Vector Machines** can assist in **cancer diagnostics** with near-expert level accuracy.

> *"In AI for health, every percentage matters. Every prediction counts."* 🌸

---

