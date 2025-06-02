# 🧠 Hand Gesture Recognition – ML Model Research

This repository contains experimental work on training and comparing different machine learning classifiers for hand gesture recognition using MediaPipe-extracted landmarks.

## 📌 Objective

Evaluate different classification algorithms using a structured MLflow pipeline to identify the best-performing model based on accuracy and F1-score.

## 📊 Dataset

The dataset includes 2D hand landmark coordinates (`x1`–`x21`, `y1`–`y21`) collected via MediaPipe and labeled with gesture classes.

## 🛠️ Models Evaluated

We trained and logged three different models using **MLflow**:

1. **K-Nearest Neighbors (KNN)**
2. **Support Vector Classifier (SVC)**
3. **XGBoost Classifier**

Each model was trained using a **grid search** over hyperparameters, with metrics and artifacts logged to MLflow.

---

## 🚀 Experiment Logging with MLflow

All training runs are tracked with:

- Model parameters
- Accuracy and macro F1-score
- Serialized models as artifacts
- Inferred input/output signatures

### 📌 Example MLflow UI Screenshots

#### ✅ KNN Runs
![KNN](https://github.com/user-attachments/assets/8f71ebdb-626d-4486-a9d2-76a2c6eec01f)


#### ✅ SVC Runs
![SVC](https://github.com/user-attachments/assets/392fd097-0c27-40fc-b4fe-c0460aba3ba6)


#### ✅ XGBoost Runs
![XGBoost](https://github.com/user-attachments/assets/1cb53752-1590-4866-bb08-5c9d1a2e57b0)


---

## ✅ Model Comparison Table

| Model   | Best Accuracy | Notes |
|---------|----------------|-------|
| KNN     | `97.74%`        | Simple, interpretable |
| SVC     | `99.66%`        | Good for high-dimensional data |
| XGBoost | `98.94%`        | Performed best overall |

> Replace the `xx.xx` placeholders with actual results from your MLflow logs.

---

## 🏆 Best Model Selected

**XGBoost** was selected as the best model based on:

- Highest **accuracy** and **F1-score** across all grid search trials.
- Strong performance even with varying hyperparameters.
- Robustness to feature scaling and noise.

---
