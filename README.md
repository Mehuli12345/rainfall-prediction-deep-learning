# 🌧️ Rainfall Prediction Using Deep Learning

This project predicts **whether it will rain tomorrow** (classification) and **how much rainfall will occur** (regression) using deep learning techniques. It uses a real-world weather dataset with various meteorological features such as temperature, humidity, pressure, and more.

---

## 📌 Problem Statement

Predicting rainfall is crucial for agriculture, urban planning, and disaster prevention. Traditional models often fall short due to the complexity of weather patterns. This project leverages deep learning to:

- Classify whether it will rain tomorrow (Yes/No)
- Predict the expected rainfall in millimeters (mm)

---

## 📊 Dataset

**Source**: [Kaggle - Rain in Australia](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package)  
**File used**: `weatherAUS.csv`

### Features (Selected):
- MinTemp, MaxTemp
- Humidity9am, Humidity3pm
- Pressure9am, Pressure3pm
- Temp9am, Temp3pm
- RainToday (Yes/No → 1/0)
- Target 1: RainTomorrow (Yes/No → Classification)
- Target 2: Rainfall (mm → Regression)

---

## 🧠 Model Architecture

Two separate deep learning models were developed using **TensorFlow/Keras**:

### 1. Classification Model
- Input: Meteorological features
- Output: Probability of rain tomorrow (sigmoid)
- Loss: Binary Crossentropy
- Metrics: Accuracy, Precision, Recall, F1 Score, MCC

### 2. Regression Model
- Input: Same as above
- Output: Predicted rainfall in mm
- Loss: Mean Squared Error (MSE)
- Metrics: Mean Absolute Error (MAE)

---

## 🧪 Evaluation

The models were evaluated using **5-Fold Cross Validation**:

### Classification Metrics:
- Accuracy
- Precision
- Recall
- F1 Score
- Matthews Correlation Coefficient (MCC)
- Confusion Matrix

### Regression Metrics:
- Mean Absolute Error (MAE)

---

## ⚙️ Preprocessing

- Dropped columns with excessive missing values
- Filled missing numeric data with mean
- Encoded categorical variables using `LabelEncoder`
- Scaled features using `StandardScaler`
- Applied `KFold(n_splits=5)` for cross-validation

---

## ✅ Results (Average across 5 folds)

| Metric               | Value        |
|----------------------|--------------|
| Accuracy             | ~89%         |
| Precision            | ~84%         |
| Recall               | ~72%         |
| F1 Score             | ~77%         |
| MCC                  | ~0.67        |
| MAE (Rainfall)       | ~1.5 mm      |




