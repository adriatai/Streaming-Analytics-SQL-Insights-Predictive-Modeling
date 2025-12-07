# 🎬 **Streaming Analytics — SQL · Machine Learning · Visualization**

### *MET AD 599 — Python & SQL (Fall 2025)*

**Team Members: Weikai Liu · Yining Chang · Yuming Zhou · Yunting Su · Yijia Tai**

---

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9+-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/SQL-DuckDB-orange?logo=database&logoColor=white" />
  <img src="https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-green?logo=scikitlearn&logoColor=white" />
  <img src="https://img.shields.io/badge/Visualization-Matplotlib%20%7C%20Seaborn-yellow?logo=chart-bar&logoColor=white" />
</p>

---

## 🧭 **Project Overview**

This project analyzes user engagement patterns on a streaming platform using **Python, SQL, Machine Learning, and Data Visualization**.
We integrate behavioral metrics, movie metadata, and temporal features to uncover insights about viewing behavior and predict movie ratings.

Our deliverables include:

* Feature engineering & behavioral analytics
* Predictive modeling (Task 3)
* Visualization & insight generation (Task 4)
* Written interpretation (Task3.docx, Task4.docx)
* Clean, reproducible code in Jupyter Notebooks

---

# 📂 **Repository Structure**

```
📁 Streaming-Analytics-Project
│
├── content.csv                 # Dataset used for analysis
│
├── Task_3.ipynb                # Machine Learning (Rating Prediction)
├── Task_4.ipynb                # Visualization & Insights
│
├── Task3.docx                  # ML model interpretation
├── Task4.docx                  # Visualization explanations
│
└── README.md                   # Project documentation (this file)
```

---

# 📊 **Dataset Summary**

The dataset contains simulated streaming platform sessions with the following major categories:

### **🎯 User Behavior**

* watch_minutes
* watch_ratio
* completed_flag
* session time (hour_of_day, day_of_week)

### **👤 User History**

* user_total_sessions
* user_completion_rate
* user_avg_watch_minutes
* user_unique_movies

### **🎬 Movie Information**

* duration_minutes
* release_year
* movie_view_count
* movie_completion_rate

### **⭐ Rating**

* target_rating (1–5) — ML prediction target

---

# 🤖 **Task 3 — Machine Learning Model**

📄 Detailed interpretation in **Task3.docx**

### **Objective**

Predict movie ratings based on behavioral and metadata features.

### **Models Implemented**

* Linear Regression
* Random Forest Regressor
* Gradient Boosting Regressor

### **Performance Summary**

| Model             | RMSE      | MAE       | R²     |
| ----------------- | --------- | --------- | ------ |
| Linear Regression | **0.890** | **0.744** | -0.001 |
| Gradient Boosting | 0.897     | 0.744     | -0.018 |
| Random Forest     | 0.908     | 0.746     | -0.042 |

📌 **Conclusion:** Ratings are highly subjective; engagement patterns are more predictable than ratings themselves.

---

## ⭐ **Top Predictive Features**

Feature importance (across all models) revealed:

1. User Average Watch Minutes
2. Watch Minutes
3. User Completion Rate
4. Watch Ratio
5. Movie Completion Rate

📌 **Insight:** Engagement level is far more important than genre, device type, or release year.

---

# 📈 **Task 4 — Visualizations & Behavioral Insights**

📄 Detailed analysis in **Task4.docx**

### **1. Viewing Duration Patterns**

Peak engagement occurs **1–2 AM**, lowest during **10–12 PM**.
➡ Optimize recommendations around peak windows.

### **2. Watch Ratio by Genre**

Genres have **stable watch ratios (≈0.70)**.
➡ Engagement is user-driven, not genre-driven.

### **3. Distribution of Watch Ratio**

Most users watch **50–90%** of a film.
➡ Supports engagement-based user segmentation.

### **4. Correlation Matrix**

Strong correlations among:

* watch_minutes
* watch_ratio
* completed_flag

Weak correlations for:

* release_year
* hour_of_day
* target_rating

➡ Ratings are weakly predictable; behaviors are strongly patterned.

### **5. Completion Rate by Device**

Ranked:

1. Mobile
2. TV
3. Web

➡ Mobile-first strategies could improve conversion.

---

# 📝 **Dependencies**

Install project dependencies via:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn duckdb
```

---

# ▶️ **How to Run**

### **Run Machine Learning Notebook**

```bash
jupyter notebook Task_3.ipynb
```

### **Run Visualization Notebook**

```bash
jupyter notebook Task_4.ipynb
```

Make sure **content.csv** is in the same folder.

---

# 🧩 **Future Improvements**

Potential extensions include:

* Completion prediction model
* Recommender system prototype
* User segmentation with clustering
* Dashboard (Plotly / Streamlit)
* Model deployment with FastAPI

---

# 👥 **Team Members**

| Name            
| ---------------- 
| **Weikai Liu**   
| **Yining Chang** 
| **Yuming Zhou** 
| **Yunting Su**  
| **Yijia Tai**  

---

# 🎓 **Acknowledgement**

Special thanks to **Sree Kumar Valath Bhuvan Das** for guidance on integrating Python, SQL, ML, and visualization techniques in real-world analytics workflows.

---
