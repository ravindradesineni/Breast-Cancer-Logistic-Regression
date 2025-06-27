# Breast-Cancer-Logistic-Regression
This project demonstrates the application of logistic regression to classify breast cancer tumors into malignant or benign categories using clinical data. It focuses on practical model development and evaluation, highlighting logistic regression’s effectiveness for binary classification tasks in healthcare scenarios.

## Project Overview

Breast cancer is among the most common cancers in women worldwide. Early detection through accurate diagnosis is critical. This machine learning project aims to create a predictive model using logistic regression that can estimate the likelihood of a tumor being malignant based on features extracted from medical imaging.

---

## Data Summary

The dataset used in this project contains 569 records with 30 numerical features derived from digitized images of fine needle aspirate (FNA) of breast masses. These features describe attributes such as radius, texture, area, and symmetry of the cell nuclei.

The target label (`diagnosis`) indicates whether a tumor is:
- **Malignant (M)**: 1
- **Benign (B)**: 0

The dataset was cleaned, preprocessed, and transformed to fit the binary classification workflow required for logistic regression.

---

## Methodology

The project is structured in the following key phases:

### 1. Data Cleaning and Preprocessing
- Removed irrelevant or redundant columns (`id`, unnamed columns).
- Encoded categorical labels into binary numerical form.
- Checked for and dropped missing values to maintain data integrity.

### 2. Feature Engineering
- Independent variables (features) and dependent variable (label) were separated.
- Applied standard scaling to the features to ensure they are on the same scale.
- Data was split into training and testing sets using a stratified approach to maintain class balance.

### 3. Model Training
- Used logistic regression as the classification algorithm.
- Fitted the model on the training data and generated probability outputs for the test set.
- Predictions were made using both class labels and class probabilities.

### 4. Evaluation Metrics
- **Confusion Matrix** was used to visualize classification performance.
- **Classification Report** provided precision, recall, F1-score, and support for both classes.
- **ROC-AUC Score** offered a quantitative measure of model discrimination power.
- A **ROC Curve** was plotted to analyze model performance across different thresholds.

### 5. Threshold Tuning
Beyond default threshold of 0.5, the model was evaluated over a range of thresholds to observe how precision and recall trade off. This is especially important in healthcare applications where false negatives can be critical. A plot of precision vs. recall across thresholds was generated.

### 6. Sigmoid Function Analysis
The sigmoid function is central to logistic regression. It maps the linear model output to a probability between 0 and 1, making it interpretable. A standalone plot was created to visualize the sigmoid curve and its behavior over various input values.

---

## Key Results and Learnings

- The model achieved a strong ROC-AUC score, indicating effective separation between malignant and benign tumors.
- Precision and recall metrics helped highlight the model’s strength in minimizing false negatives (malignant predicted as benign).
- Threshold tuning gave more flexibility in adjusting the model's sensitivity based on real-world risk tolerance.
- The sigmoid visualization reinforced the mathematical foundation of logistic regression’s probabilistic output.

---

## How to Execute the Project

1. Open the Jupyter Notebook file provided (`code(Task4).ipynb`).
2. Ensure the CSV dataset file is in the same directory.
3. Execute the cells in sequence to perform preprocessing, modeling, evaluation, and visualization.
4. Review the output metrics and plots for interpretation and insights.

---

## Conclusion

This project demonstrates how logistic regression, when combined with thoughtful data processing and evaluation, can provide actionable insights in binary classification problems like cancer diagnosis. The model is simple, interpretable, and extendable, making it a solid baseline for more complex approaches in medical AI applications.
