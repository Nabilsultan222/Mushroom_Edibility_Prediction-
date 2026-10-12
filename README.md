# Mushroom_Edibility_Prediction-
# 🍄 Mushroom Classification: Edible vs. Poisonous

This project implements and compares various machine learning models to classify mushrooms as either **edible (e)** or **poisonous (p)** based on their physical features.

## 📋 Project Overview
- **Objective:** Build a robust classifier to identify toxic mushrooms with high accuracy to prevent potential poisoning.
- **Dataset:** 8,124 samples of mushrooms, containing 22 categorical features (e.g., cap-shape, odor, gill-color).
- **Target Class:** Binary (`class`: Edible=0, Poisonous=1 after encoding).

## 🛠️ Workflow & Key Steps

### 1. Data Cleaning & Preprocessing
- **Handling Missing Values:** Replaced missing values (`?`) in the `stalk-root` column with its statistical mode.
- **Feature Selection:** Dropped the `veil-type` feature since it contained only a single unique value (`p`), offering zero variance or predictive value.
- **Categorical Encoding:** Applied `LabelEncoder` to transform all categorical feature categories and the target variable into numerical representations.
- **Splitting:** Split the preprocessed dataset into **70% Training** and **30% Testing** subsets.

### 2. Model Implementation
We implemented and benchmarked six different machine learning algorithms to compare performance:
- **Gaussian Naive Bayes**
- **Decision Tree Classifier**
- **Random Forest Classifier**
- **K-Nearest Neighbors (KNN)**
- **Support Vector Machine (SVM)**
- **Multilayer Perceptron (MLP Neural Network)**

---

## 📊 Comparative Performance Results

Our models achieved outstanding predictive performance, with non-linear models showing near-perfect classification capabilities:

| Model | Accuracy | ROC-AUC Score | F1-Score (Class 1) |
| :--- | :---: | :---: | :---: |
| **Multilayer Perceptron (MLP)** | **99.92%** | **1.0000** | **1.00** |
| **K-Nearest Neighbors (KNN)** | **99.63%** | **1.0000** | **1.00** |
| **Support Vector Machine (SVM)** | **99.02%** | **0.9998** | **0.99** |
| **Random Forest** | **98.93%** | **0.9998** | **0.99** |
| **Decision Tree** | **95.32%** | **0.9822** | **0.95** |
| **Naive Bayes** | **90.44%** | **0.9528** | **0.90** |

### 🔑 Insights
- **Top Performers:** The Multi-layer Perceptron (MLP Neural Network) and KNN achieved near-perfect accuracy and perfect Area Under the ROC Curve (1.00).
- **Most Important Features:** Correlation analysis and tree models showed that attributes like `odor`, `gill-size`, and `gill-color` had strong relationships with mushroom toxicity.

---

## 💻 Technologies Used
- **Language:** Python 3
- **Core Libraries:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Machine Learning:** `scikit-learn`
