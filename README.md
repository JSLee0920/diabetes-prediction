# Diabetes Prediction Project

## Project Overview

This project focuses on building a predictive model to identify the likelihood of diabetes in patients based on clinical and demographic features. By utilizing machine learning and deep learning techniques, the project evaluates and compares different algorithms to find the most effective approach for early diagnosis.

## Dataset Description

The analysis is based on a clinical dataset containing various health indicators.

- **Source File:** `diabetes_dataset_with_notes.csv`
- **Total Records:** 100,000 entries (initially)
- **Key Features:**
  - `gender`: Patient gender (includes Female, Male, and Other)
  - `age`: Patient age
  - `hypertension`: Blood pressure status (0 or 1)
  - `heart_disease`: Presence of heart conditions (0 or 1)
  - `smoking_history`: History of tobacco use (e.g., never, current, former, No Info)
  - `bmi`: Body Mass Index
  - `HbA1c_level`: Hemoglobin A1c levels
  - `blood_glucose_level`: Blood sugar levels
  - **Target Variable (`diabetes`)**: 0 (Negative) or 1 (Positive)

---

## Methodology

### 1. Data Exploration & Cleaning

- **Feature Engineering:** Dropped non-predictive columns including `year`, `location`, `race` sub-categories, and `clinical_notes`.
- **Missing Value Handling:** Addressed records with "No Info" in smoking history.
- **Outlier Detection:** Used the Interquartile Range (IQR) method to identify extreme BMI values (Upper bound: ~38.5, Lower bound: ~14.7).
- **Duplicate Removal:** Removed 3,854 duplicate rows to ensure data integrity.

### 2. Preprocessing

- **Encoding:** Converted categorical data (gender, smoking_history) into numerical formats.
- **Scaling:** Applied standard scaling to numeric features for models like SVM and Neural Networks.

### 3. Models Evaluated

- **Random Forest Classifier**
- **Support Vector Machine (SVM)**
- **Decision Tree Classifier**
- **TensorFlow Deep Neural Network (DNN)**
- **Recurrent Neural Network (RNN)**

---

## Results and Evaluation

The performance of each model was measured using **Accuracy** and **F1-Score**.

| Model             | Accuracy  |  F1-Score  |
| :---------------- | :-------: | :--------: |
| **Random Forest** | **96.1%** |   0.801    |
| **Decision Tree** |   96.0%   | **0.8011** |
| **SVM**           |   95.7%   |   0.775    |

**Key Findings:**

- The **Decision Tree** model provided the highest F1-Score, making it highly effective at balancing precision and recall for this dataset.
- **Random Forest** showed strong performance with high accuracy and robustness against overfitting.

---

## Getting Started

### Prerequisites

You will need Python 3.x and the following libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow
```
