# Wine Quality Prediction using Machine Learning

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange.svg)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-Latest-green.svg)](https://xgboost.readthedocs.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A professional machine learning project focused on predicting wine quality based on physicochemical properties. This repository demonstrates a complete ML workflow, from data exploration and preprocessing to model training and evaluation.

## 🍷 Project Overview

Wine quality is typically assessed by sensory evaluations, which can be subjective and time-consuming. This project leverages **supervised machine learning** to build a classification model that predicts whether a wine is of "good quality" based on its chemical composition. By identifying the key features that influence quality, we can provide objective insights for winemakers and distributors.

## 📊 Problem Statement

The goal is to classify wines into two categories (e.g., Good vs. Not Good) based on various chemical attributes. This is a **binary classification problem** where we aim to maximize predictive accuracy and robustness across different wine types (Red and White).

## 🗃️ Dataset Description

The project uses the **Wine Quality Dataset**, which contains information on both red and white variants of the Portuguese "Vinho Verde" wine.

- **Instances:** 6,497 samples
- **Attributes:** 11 physicochemical features + 1 target variable (Quality)
- **Target Variable:** `quality` (score between 0 and 10, later binarized for classification)

### Key Features:
- **Acidity:** Fixed acidity, Volatile acidity, Citric acid
- **Composition:** Residual sugar, Chlorides, Free sulfur dioxide, Total sulfur dioxide, Density
- **Chemical Balance:** pH, Sulphates, Alcohol
- **Type:** Red or White wine

## ⚙️ Machine Learning Workflow

1. **Exploratory Data Analysis (EDA):** Visualizing distributions, handling missing values, and identifying correlations using `seaborn` and `matplotlib`.
2. **Preprocessing:** 
   - Feature engineering (e.g., binarizing the quality score).
   - Handling class imbalance.
   - Feature scaling using `MinMaxScaler`.
3. **Model Selection:** Comparing multiple classification algorithms.
4. **Evaluation:** Assessing performance using ROC AUC score and classification reports.

## 🤖 Models Used

The following algorithms were implemented and compared:
- **Logistic Regression:** A baseline linear model for classification.
- **Support Vector Classifier (SVC):** Effective in high-dimensional spaces.
- **XGBoost Classifier:** A powerful gradient boosting framework for optimized performance.

## 📈 Results Summary

The models were evaluated using the **ROC AUC Score** to measure their ability to distinguish between classes:

| Model | Training ROC AUC | Validation ROC AUC |
| :--- | :--- | :--- |
| **XGBoost** | **0.976** | **0.805** |
| **SVC** | 0.720 | 0.707 |
| **Logistic Regression** | 0.708 | 0.694 |

*XGBoost demonstrated superior performance, achieving a high training accuracy, though showing some signs of overfitting that could be addressed in future iterations.*

## 💡 What You Will Learn
- How to handle multi-source datasets (Red and White wine).
- Techniques for data visualization and correlation analysis.
- Implementation of advanced boosting algorithms like XGBoost.
- Best practices for evaluating classification models using ROC AUC.

## 🚀 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/SOUGUR/Wine_Quality_Prediction_Machine_Learning.git
   cd Wine_Quality_Prediction_Machine_Learning
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## 💻 How to Run

1. Navigate to the `notebooks/` directory.
2. Launch Jupyter Notebook or JupyterLab:
   ```bash
   jupyter notebook
   ```
3. Open `Wine_Quality_Prediction_Machine_Learning.ipynb` and run all cells.

## 🛠️ Future Improvements
- **Hyperparameter Tuning:** Implement GridSearchCV or RandomizedSearchCV to optimize XGBoost.
- **Cross-Validation:** Use K-Fold cross-validation for more robust performance estimation.
- **Feature Importance:** Analyze and visualize which chemical properties most significantly impact wine quality.
- **Deployment:** Create a simple web app using Streamlit to allow users to input chemical values and get quality predictions.

---
**Author:** [SOUGUR](https://github.com/SOUGUR)  
**License:** MIT
