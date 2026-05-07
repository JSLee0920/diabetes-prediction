# Diabetes Prediction Project

## Project Overview
This project focuses on building a predictive model to identify the likelihood of diabetes in patients based on clinical and demographic features. By utilizing machine learning and deep learning techniques, the project evaluates and compares different algorithms to find the most effective approach for early diagnosis.

This project was developed by **1E Group 3**:
*   **Lee Jia Sheng**
*   **Yeo Zing Le**[cite: 1]
*   **Soo Kian Sheng**[cite: 1]
*   **Ng Yee Hng**[cite: 1]

---

## Dataset Description
The analysis is based on a clinical dataset containing various health indicators[cite: 1].
*   **Source File:** `diabetes_dataset_with_notes.csv`[cite: 1]
*   **Total Records:** 100,000 entries (initially)[cite: 1]
*   **Key Features:**
    *   `gender`: Patient gender (includes Female, Male, and Other)[cite: 1]
    *   `age`: Patient age[cite: 1]
    *   `hypertension`: Blood pressure status (0 or 1)[cite: 1]
    *   `heart_disease`: Presence of heart conditions (0 or 1)[cite: 1]
    *   `smoking_history`: History of tobacco use (e.g., never, current, former, No Info)[cite: 1]
    *   `bmi`: Body Mass Index[cite: 1]
    *   `HbA1c_level`: Hemoglobin A1c levels[cite: 1]
    *   `blood_glucose_level`: Blood sugar levels[cite: 1]
    *   **Target Variable (`diabetes`)**: 0 (Negative) or 1 (Positive)[cite: 1]

---

## Methodology

### 1. Data Exploration & Cleaning
*   **Feature Engineering:** Dropped non-predictive columns including `year`, `location`, `race` sub-categories, and `clinical_notes`[cite: 1].
*   **Missing Value Handling:** Addressed records with "No Info" in smoking history[cite: 1].
*   **Outlier Detection:** Used the Interquartile Range (IQR) method to identify extreme BMI values (Upper bound: ~38.5, Lower bound: ~14.7)[cite: 1].
*   **Duplicate Removal:** Removed 3,854 duplicate rows to ensure data integrity[cite: 1].

### 2. Preprocessing
*   **Encoding:** Converted categorical data (gender, smoking_history) into numerical formats[cite: 1].
*   **Scaling:** Applied standard scaling to numeric features for models like SVM and Neural Networks[cite: 1].

### 3. Models Evaluated
*   **Random Forest Classifier**[cite: 1]
*   **Support Vector Machine (SVM)**[cite: 1]
*   **Decision Tree Classifier**[cite: 1]
*   **TensorFlow Deep Neural Network (DNN)**[cite: 1]
*   **Recurrent Neural Network (RNN)**[cite: 1]

---

## Results and Evaluation
The performance of each model was measured using **Accuracy** and **F1-Score**[cite: 1].

| Model | Accuracy | F1-Score |
| :--- | :---: | :---: |
| **Random Forest** | **96.1%** | 0.801 |
| **Decision Tree** | 96.0% | **0.8011** |
| **SVM** | 95.7% | 0.775 |

**Key Findings:**
*   The **Decision Tree** model provided the highest F1-Score, making it highly effective at balancing precision and recall for this dataset[cite: 1].
*   **Random Forest** showed strong performance with high accuracy and robustness against overfitting[cite: 1].

---

## Getting Started

### Prerequisites
You will need Python 3.x and the following libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow
