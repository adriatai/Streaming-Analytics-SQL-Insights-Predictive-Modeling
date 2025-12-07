# 🎬 Streaming Platform Analytics

### **Machine Learning · Visualization · Behavioral Insights**

---

## 👥 **Team Members**

* **Weikai Liu**
* **Yining Chang**
* **Yuming Zhou**
* **Yunting Su**
* **Yijia Tai**

---

## 📌 **Project Overview**

This repository contains the implementation for:

* **Task 3:** Machine Learning Model for Movie Rating Prediction
* **Task 4:** Data Visualizations & Business Insights

The goal of this project is to **predict user movie ratings and understand factors that affect user engagement and completion behaviors** on a streaming platform.

---

# 🧠 **Task 3 — Machine Learning Model**

## 🎯 Objective

Predict user movie ratings (1–5) using:

* Viewing behavior
* User historical metrics
* Movie attributes
* Engagement indicators

📄 Detailed results cited from: Task3.docx 

---

## 🔧 **Models Implemented**

* **Linear Regression (baseline)**
* **Random Forest Regressor**
* **Gradient Boosting Regressor**

---

## 📊 **Model Performance Summary**

| Model             | RMSE      | MAE       | R²     |
| ----------------- | --------- | --------- | ------ |
| Linear Regression | **0.890** | **0.744** | -0.001 |
| Gradient Boosting | 0.897     | 0.744     | -0.018 |
| Random Forest     | 0.908     | 0.746     | -0.042 |

📌 **Insight:**
R² ≈ 0 indicates movie ratings are **highly subjective** and difficult to predict solely from behavior and metadata.

---

## ⭐ **Key Factors Influencing Predictions**

Feature importance ranking shows engagement metrics dominate:

* User Average Watch Minutes — **9.1%**
* Watch Minutes — **9.1%**
* User Completion Rate — **8.9%**
* Watch Ratio — **8.8%**
* Movie Completion Rate — **8.0%**

📌 Device type, age rating, genre = low influence.
📌 “Completed or not” flag is less predictive than **continuous watch_ratio**.

---

## 📝 **Task 3 Conclusion**

* User ratings are influenced more by *personal preference* than behavioral metrics.
* Engagement level (how long users watch) is a strong predictor of rating behavior.
* Platforms should focus on improving viewing engagement to influence satisfaction.

---

# 📊 **Task 4 — Visualizations & Insights**

📄 Based on: Task4.docx 

Task 4 includes **six analytical visualizations** that explain user behavior patterns.

---

## 📈 **1. Average Watch Minutes by Hour of Day**

* Viewing peaks at **1–2 AM**, dips around **10 AM–12 PM**
* Engagement rises again after **3 PM**

📌 *Business implication:*
Schedule recommendations or promotions during high-engagement windows.

---

## 🎭 **2. Average Watch Ratio by Genre**

* All genres show high watch ratios (~0.70–0.72)
* Genre has **minimal impact** on completion

📌 *Implication:* Recommendation should be **user-preference–based**, not genre-based.

---

## 🧩 **3. Distribution of Watch Ratio**

* Users show diverse viewing behaviors
* Majority watch **50%–90%** of films
* Watch ratio >1.0 appears due to rewinding or replay

📌 *Implication:*
Segment users into high-, medium-, and low-engagement groups for personalization.

---

## 🔥 **4. Correlation Matrix of Numeric Features**

Key findings:

* Strong correlations among: watch_minutes, watch_ratio, completed_flag
* Moderate correlations among user behavior aggregates
* Movie metadata & time variables weakly correlated with engagement
* target_rating correlates weakly with behavioral features

📌 *Implication:*
Engagement metrics are reliable predictors; metadata is less impactful.

---

## 🧠 **5. Feature Importances for Predicting Completion**

* **watch_ratio dominates massively**
* All other features contribute marginally

📌 *Implication:*
Early watch ratio can be used to **detect dropout risk** in real time.

---

## 📱 **6. Completion Rate by Device Type**

Completion rates (highest → lowest):

1. **Mobile**
2. **TV**
3. **Web**

📌 *Implication:*
Mobile-focused content strategy may increase completion rates.

---

# 🚀 **Technical Stack**

* Python
* Pandas / NumPy
* Scikit-Learn
* Matplotlib / Seaborn
* Jupyter Notebook

---

# ▶️ **How to Run**

### Run ML model (Task 3)

```bash
jupyter notebook Task_3.ipynb
```

### Run visualizations (Task 4)

```bash
jupyter notebook Task_4.ipynb
```

Outputs will be generated and saved locally.

---

# 🧩 **Key Business Takeaways**

* Engagement metrics (watch time, ratio) matter far more than content metadata.
* User ratings are difficult to predict due to subjective preference.
* Early behavior signals (watch_ratio) can guide **real-time interventions**.
* Device usage influences completion likelihood—optimize UX accordingly.

---


