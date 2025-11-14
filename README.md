
# 🍽️ Calorie Expenditure Prediction

### *Mini Machine Learning Experiment — EONVERSE AI Intern Screening Challenge*

### *By Debanuj Roy*

---

## 📌 **Project Overview**

This project predicts **calorie expenditure** using physiological and activity-related features.
It was developed as part of the **EONVERSE AI Intern – Screening Challenge**, under the **Option 1: Mini Machine Learning Experiment** track.

The experiment uses a dataset from the **Kaggle Playground Series – Season 5, Episode 5**, applies **feature engineering**, **preprocessing**, and trains an **XGBoost regression model** with **15-fold cross-validation**.
The final model achieves:

* **Public Leaderboard Score:** `0.05809`
* **Private Leaderboard Score:** `0.05978`

---

## 🚀 **Features of This Project**

* Complete ML pipeline using **scikit-learn + XGBoost**
* Automatic **feature engineering** (BMI + interaction terms)
* Robust **preprocessing pipeline** (scaling + encoding)
* **15-Fold cross-validation** for stable metrics
* Log-transformed regression target for performance stability
* End-to-end **submission generator** (`submission.csv`)
* Visualizations:

  * Correlation heatmap
  * Feature importance
  * Distributions

---

## 📁 **Repository Structure**

```
📦 Calorie-Expenditure-Prediction
├── calorie_prediction.py       # Main ML script (Colab notebook converted to .py)
├── submission.csv              # Final Kaggle submission (optional)
├── README.md                   # Project documentation
├── report.pdf / report.tex     # EONVERSE submission report (if included)
└── assets/
       ├── leaderboard.png      # Kaggle leaderboard screenshot
       └── workflow.png         # Workflow diagram (optional)
```

---

## 📊 **Dataset**

The dataset comes from Kaggle:

👉 **Predict Calorie Expenditure — Playground Series S5 E5**
Link: [https://www.kaggle.com/competitions/playground-series-s5e5](https://www.kaggle.com/competitions/playground-series-s5e5)

**Input features include:**

* Heart Rate
* Body Temperature
* Height & Weight
* Activity Duration
* Other sensor/activity measurements

**Target variable:**
`Calories` — calories burned during activity.

---

## 🔧 **Tech Stack & Libraries**

* **Python 3.10+**
* **NumPy**, **Pandas**
* **Scikit-Learn**
* **XGBoost**
* **Matplotlib**, **Seaborn**
* **Google Colab**
* **Kaggle API** (optional)

---

## 🧠 **Modeling Approach**

### **1. Data Preprocessing**

* Remove duplicates
* Missing value analysis
* Standard scaling for numerical features
* One-hot encoding for categorical features

### **2. Feature Engineering**

* BMI computation:
  [
  BMI = \frac{\text{Weight}}{(\text{Height}/100)^2}
  ]
* Cross-features for numerical variables (pairwise multiplication)

### **3. Model**

* **XGBRegressor**
* Key parameters:

  ```
  max_depth=10
  learning_rate=0.02
  n_estimators=2000
  colsample_bytree=0.75
  subsample=0.9
  gamma=0.01
  early_stopping_rounds=100
  ```

### **4. Validation**

* **15-Fold KFold Cross-Validation**
* RMSE computed on **log-transformed** target (`log1p`)

### **5. Submission**

The script produces:

```
submission.csv
```

Format:

| id | Calories |
| -- | -------- |

Ready for Kaggle upload.

---

## 🖼️ **Results**

### **Leaderboard Performance**

| Type    | Score     |
| ------- | --------- |
| Public  | `0.05809` |
| Private | `0.05978` |

Leaderboard screenshot is included in the `assets/` directory.

---

## 📽️ **Demo Video**

As required by the EONVERSE challenge, a demo video explaining the approach and results is included:

👉 *(Add your link here once uploaded)*

---

## 📄 **Report**

Complete 2–3 page detailed report (LaTeX + compiled PDF) for the EONVERSE evaluation:

* Workflow
* Code explanation
* Feature engineering
* Results & Learnings
* Improvements

👉 See `report.tex` / `report.pdf` in this repo.

---

## 🛠️ **How to Run**

### **1. Install Dependencies**

```bash
pip install -r requirements.txt
```

(Or install manually: numpy, pandas, scikit-learn, xgboost, seaborn, matplotlib)

### **2. Run Training + Generate Submission**

```bash
python calorie_prediction.py
```

### **3. Output**

A ready-to-submit file will appear:

```
submission.csv
```

---

## 🔮 **Future Improvements**

* Hyperparameter search using Optuna
* SHAP-based interpretability
* LightGBM / CatBoost ensembling
* Streamlit app for calorie prediction
* Automated feature selection

---

## 🤝 **Contributing**

Contributions and pull requests are welcome!
If you'd like to improve the model, add more plots, or optimize hyperparameters — feel free to contribute.

---

## 📬 Contact

For queries or collaboration:

**Debanuj Roy**
Email: <a href="debanujroy1234@gmail.com">debanujroy1234@gmail.com</a>
LinkedIn: <a href="www.linkedin.com/in/debanuj-roy-b3709b275">www.linkedin.com/in/debanuj-roy-b3709b275</a> 


Just tell me!
