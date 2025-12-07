# 📊 **Streaming Analytics & Predictive Modeling**

### *Machine Learning · Exploratory Data Analysis · Visualization*

**MET AD 699 – Data Mining for Business Analytics**

---

## 🧭 **Project Overview**

This repository contains the implementation for **Task 3 (Machine Learning Model)** and **Task 4 (Visualizations & Insights)** of a streaming-platform analytics project.
Using behavioral, contextual, and content-level features, we develop predictive models to estimate **user movie ratings**, alongside visual analytics to extract actionable business insights.

The workflows reflect real-world data mining practices:

* Robust data preprocessing & feature engineering
* Baseline + advanced ML model development
* Model performance benchmarking
* Interpretability through feature importance
* Executive-ready visual insights for business strategy

---

## 📂 **Repository Structure**

```
├── Task_3.ipynb                # Machine Learning pipeline (full workflow)
├── Task_4.ipynb                # Visualization & exploratory insights
├── content.csv                 # Input dataset (behavior + metadata)
├── model_comparison.csv        # Performance metrics across models
├── feature_importance.csv      # Ranked feature importance table
├── feature_importance.png      # Feature importance bar plot
└── README.md                   # Project documentation
```

---

## ⚙️ **Environment Setup**

### Python Version

> Python 3.9+

### Install Required Libraries

```bash
pip install numpy pandas scikit-learn matplotlib seaborn
```

---

# 🧹 **Task 3 — Machine Learning Model**

## 1️⃣ Data Preprocessing

Key steps implemented:

* Handling missing values
* Removing duplicate interactions
* Encoding categorical variables (genre, device type, age rating)
* Rescaling features for linear models
* 17 engineered predictors integrating:

  * user engagement behavior
  * content metadata
  * contextual viewing patterns

Example preprocessing block:

```python
df = pd.read_csv("content.csv")
df.dropna(inplace=True)
df = df.drop_duplicates(subset="rating_id")
```

---

## 2️⃣ Feature Engineering

The model uses a robust behavioral feature set, including:

| Feature Category        | Examples                                      |
| ----------------------- | --------------------------------------------- |
| **User Engagement**     | watch_minutes, watch_ratio, completion_rate   |
| **User History**        | user_avg_watch_minutes, user_genre_pref_score |
| **Content Metadata**    | release_year, duration_minutes, genre_encoded |
| **Contextual Features** | hour_of_day, day_of_week                      |

These features support high-quality predictive modeling aligned with industry best practices.

---

## 3️⃣ Model Development

### ✔ Baseline Model

* **Linear Regression**

### ✔ Advanced Models

* **Random Forest Regressor**
* **Gradient Boosting Regressor**

All models are trained using the same train-test split for fair evaluation.

---

## 4️⃣ Evaluation Metrics

We compute standard regression metrics:

* **RMSE** — penalizes large errors
* **MAE** — average prediction deviation
* **R² Score** — variance explained

Results are saved into:

```
model_comparison.csv
```

Example format:

| Model             | RMSE | MAE  | R²   |
| ----------------- | ---- | ---- | ---- |
| Linear Regression | 0.XX | 0.XX | 0.XX |
| Random Forest     | 0.XX | 0.XX | 0.XX |
| Gradient Boosting | 0.XX | 0.XX | 0.XX |

The best-performing model is chosen based on **RMSE minimization**.

---

## 5️⃣ Feature Importance Analysis

Feature importance from Random Forest is exported as:

```
feature_importance.csv
feature_importance.png
```

This ranking highlights **what drives rating predictions**, typically:

* user engagement duration
* completion ratio
* historical viewing affinity
* movie metadata (secondary influence)

These insights guide recommendation and content strategy decisions.

---

# 📊 **Task 4 — Visualizations & Insights**

Task 4 generates a suite of at least **six analytical plots** designed for executive-level reporting.

### 📈 1. Time Series Trend

Longitudinal patterns in viewing behavior.
### Average Watch Minutes by Hour of Day
![Average Watch Minutes](/mnt/data/a4f9da65-7de2-4b5a-8eab-9f0c71e54e32.png)


### 📊 2. Distribution Analysis

Watch minutes, rating distribution, engagement patterns.
### Average Watch Ratio by Genre
![Average Watch Ratio](/mnt/data/99841222-dc31-424f-a7f7-f32277b292e2.png)


### 🧩 3. Category Comparison (Bar Charts)

Top genres, device usage frequency, peak viewing hours.
### Distribution of Watch Ratio
![Watch Ratio Distribution](/mnt/data/ef15c4e5-3bd6-4c9e-99ea-ab090324ddbe.png)


### 🔥 4. Correlation Heatmap

Identifying multicollinearity and feature clusters.
### Correlation Matrix of Numeric Features
![Correlation Matrix](/mnt/data/b5ca83a7-d853-4b65-9624-fd54f941c2ef.png)


### 🧠 5. Machine Learning Interpretability

* Feature importance visualization
* Error distributions
* Model comparison plots
### Top 10 Feature Importances for Predicting Completion
![Feature Importances](/mnt/data/a18d7e4e-c742-48a1-b83d-fba8c7f00e22.png)


### 🎬 6. Domain-Specific Visualization

Illustrates streaming-specific phenomena such as drop-off curves or binge-session patterns.
### Average Completion Rate by Device Type
![Completion Rate by Device](/mnt/data/ca4a9ad0-f39c-4abe-9900-5b4ff6c9859a.png)


---

# 💡 **Key Business Insights**

From the analysis:

### 1️⃣ User engagement behavior is the strongest driver of rating outcomes

Features like *watch_minutes* and *completion_rate* outperform all content metadata.

### 2️⃣ Viewing context (hour, device) exhibits moderate predictive influence

Recommendation engines may adjust ranking by context-aware personalization.

### 3️⃣ Genre metadata alone is not highly predictive

Behavior > metadata — consistent with commercial recommender system findings.

### 4️⃣ Advanced models (RF/GB) significantly outperform linear models

Tree-based models capture nonlinear user behaviors and interaction effects.

---

# ▶️ **How to Run**

### Run Machine Learning Workflow

```bash
jupyter notebook Task_3.ipynb
```

### Run Visual Analytics

```bash
jupyter notebook Task_4.ipynb
```

Generated outputs (plots + CSVs) will be saved locally.

---

# 👥 **Authors**

**Team Members**

*  Weikai Liu
*  Yining Chang
*  Yuming Zhou
*  Yunting Su
*  Yijia Tai


**Course:** MET AD 699 – Data Mining for Business Analytics
**Institution:** Boston University Metropolitan College

---

# 🏁 **Next Steps (Optional Extensions)**

Future enhancements could include:

* Hyperparameter tuning (GridSearch / RandomSearch)
* XGBoost or LightGBM modeling
* Deployment via Flask / FastAPI
* Real-time streaming analytics with Spark / Kafka
* Production-grade recommendation engine

