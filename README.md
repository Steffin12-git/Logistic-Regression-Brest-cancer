# 🩺 Logistic Regression — Breast Cancer Classification

**Repository:** *Logistic Regression Breast Cancer*
**Notebook:** `Logistic Regression Breast Cancer.ipynb`

---

## 🚀 Tech Stack

![Python](https://img.shields.io/badge/Python-3.9-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-yellow?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?logo=scikitlearn)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green?logo=matplotlib)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-lightblue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

---

## 🎯 Objective

Develop an interpretable **Logistic Regression** model to classify breast tumors as **benign or malignant** based on diagnostic features. The project demonstrates the **end-to-end ML workflow**: preprocessing, EDA, modeling, evaluation, and interpretation.

---

## ⚡ Pitch 

Built and validated a **Logistic Regression model** achieving **98% accuracy** with high recall for malignant tumors — interpretable, lightweight, and production-ready for healthcare analytics use cases.

---

## 📊 Dataset

* **Source:** Breast Cancer Wisconsin (Diagnostic) dataset (569 samples, 30 features).
* **Preprocessing:**

  * Removed `id` and `Unnamed: 32`.
  * Encoded target: `diagnosis` → Malignant = 1, Benign = 0.
  * Standardized features with `StandardScaler`.
* **Split:** 70% training / 30% testing (`random_state=42`).

---

## 🔍 Exploratory Data Analysis

* **Class balance:**
  ![Diagnosis Count](images/Daiginosis%20count.png)

* Features describe tumor cell nucleus morphology: radius, texture, smoothness, concavity, fractal dimension, etc.

* Clear separation of malignant vs benign observed in **size/concavity features**.

---

## 🧑‍💻 Modeling

* **Algorithm:** Logistic Regression (`scikit-learn`)
* **Target:** Malignant (1) / Benign (0)
* **Features:** All 30 standardized predictors
* **Metrics:** Accuracy, Precision, Recall, F1, ROC-AUC

---

## ✅ Results

### Confusion Matrix

![Confusion Matrix](images/confusion%20metrix%20actual%20vs%20prediction%20\(fp%2C%20tp\).png)

* **Accuracy:** 0.98
* **Precision (Malignant):** 0.97
* **Recall (Malignant):** 0.98
* **F1 Score (Malignant):** 0.98

👉 The model misclassified **only 1 malignant case out of 63**, minimizing false negatives (critical in healthcare).

---

### ROC Curve

![ROC Curve](images/ROC%20curve.png)

* ROC-AUC ≈ **1.0** → excellent class separability.

---

## 🔑 Feature Importance

Logistic Regression coefficients show key predictors:

* **Positive (↑ Malignancy odds):**

  * `texture_worst`, `radius_se`, `symmetry_worst`, `concave points_mean`, `concavity_worst`

* **Negative (↓ Malignancy odds):**

  * `fractal_dimension_se`, `compactness_se`, `compactness_mean`, `symmetry_se`

📌 *Clinical insight*: Tumor **concavity, texture, and size variability** are highly predictive of malignancy.

---

## ⚠️ Limitations

* Used single train/test split — **k-fold CV** recommended.
* Logistic regression assumes linear separability.
* Dataset moderately balanced → real-world external validation needed.

---

## 📈 Next Steps

1. Apply **cross-validation** for robust generalization.
2. Perform **hyperparameter tuning** (`C`, penalty type).
3. Add **calibration curves** for probability thresholds.
4. Deploy via **Flask/Django API** or **Streamlit demo**.
5. Enhance explainability with **SHAP/LIME**.

---

## ▶️ How to Reproduce

```bash
# Clone repository
git clone <your-repo-url>
cd Logistic-Regression-Breast-cancer

# Install dependencies
pip install -r requirements.txt

# Run notebook
jupyter notebook "Logistic Regression Breast Cancer.ipynb"
```

---

## 💡 Highlights

* Achieved **98% accuracy** and **98% recall for malignant detection**.
* Interpretable model with **clinically relevant features** (concavity, texture, size).
* Full ML workflow: **EDA → preprocessing → modeling → evaluation → interpretation**.
* Built with **Python, Pandas, scikit-learn, Matplotlib, Seaborn, Jupyter**.

