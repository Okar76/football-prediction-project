# ⚽ Serie A Match Outcome Prediction Project

## 🧠 Overview

This project analyzes **Serie A football match data** to build machine learning models that predict match outcomes: **Win, Draw, or Loss**.

It compares the performance of three models:
- **Decision Tree**
- **Random Forest**
- **Stacking Ensemble Classifier**

The **Stacking Ensemble** achieved the best overall accuracy and balance between precision and recall.

---

## 🚀 Key Features

### 📊 Data Processing

- Loads data from `matches_serie_A.csv`
- Removes irrelevant columns: `Notes`, `Attendance`, `Date`, `Time`
- Handles missing values
- Removes outliers using **Interquartile Range (IQR)** method

### ⚙️ Feature Engineering

- Parses team formations into numeric features:  
  `Def`, `Mid`, `Att`, `Length`
- Creates **seasonal features** from match dates:  
  `Winter`, `Spring`, `Summer`, `Autumn`
- Extracts opponent formation features:  
  `Opp_Def`, `Opp_Mid`, `Opp_Att`, `Opp_Length`

### 🤖 Model Comparison

| Model             | Accuracy | Notes                                                                 |
|------------------|----------|-----------------------------------------------------------------------|
| Decision Tree     | 47%      | Baseline model                                                       |
| Random Forest     | 54.7%    | Tuned with `GridSearchCV`                                            |
| Stacking Ensemble | **55.6%**| Combines Random Forest + Gradient Boosting with Logistic Regression |

---

## 📈 Results Summary

| Model             | Accuracy | Precision | Recall | F1 Score |
|------------------|----------|-----------|--------|----------|
| Decision Tree     | 47%      | 0.48      | 0.47   | 0.47     |
| Random Forest     | 54.7%    | 0.53      | 0.55   | 0.53     |
| Stacking Ensemble | **55.6%**| 0.53      | 0.56   | 0.52     |

---

## 💾 Requirements

- Python 3.7+
- Jupyter Notebook

### 📦 Libraries

```bash
pandas
numpy
scikit-learn
```

---

## 🧪 How to Use

1. Place `matches_serie_A.csv` in the project folder.
2. Open and run `project.ipynb` **sequentially** in Jupyter Notebook.
3. The notebook will:
   - Load and preprocess the data
   - Train and evaluate all three models
   - Display accuracy scores and classification reports

---

## 🌱 Future Improvements

- Incorporate **player statistics** and **team rankings**
- Add **real-time betting odds** for better context
- Experiment with **neural networks** for complex pattern learning
- Perform **feature importance analysis** for model explainability

---


