# TRONIXIA_ML_05
# Credit Card Fraud Detection using Machine Learning

## Overview
This project focuses on detecting fraudulent credit card transactions using supervised machine learning techniques. The dataset is highly imbalanced, making fraud detection a challenging real-world problem.

The goal is to build a robust classification pipeline that can effectively identify fraudulent transactions while minimizing false negatives.

---

## Dataset
- Dataset: Credit Card Fraud Detection Dataset
- Total transactions: 284,807
- Fraud cases: ~0.17%
- Features: PCA-transformed variables (V1–V28), Amount, Time
- Target variable: `Class`
  - 0 → Normal transaction
  - 1 → Fraudulent transaction

Due to file size limitations, the dataset is not included in this repository.

You can download it from:
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

---

## Methodology

### 1. Data Preprocessing
- Removed `Time` column (not useful for prediction)
- Scaled `Amount` feature using StandardScaler
- Used PCA-transformed features (V1–V28) as provided

### 2. Handling Class Imbalance
- Dataset is highly imbalanced (~0.17% fraud)
- Used `class_weight='balanced'` in models
- Applied stratified train-test split to maintain class distribution

### 3. Model Training
Two classification models were implemented:

- Logistic Regression (baseline model)
- Random Forest Classifier (ensemble model)

### 4. Evaluation Metrics
Due to imbalance, accuracy is not reliable. Models were evaluated using:

- Precision
- Recall
- ROC-AUC Score
- Confusion Matrix

---

## Results

- Both models demonstrated strong performance in fraud detection
- Random Forest showed better capability in capturing complex patterns
- High recall is critical to minimize missed fraud cases

---

## Key Insights

- Class imbalance significantly affects model performance
- Recall is more important than accuracy in fraud detection
- Proper preprocessing and evaluation metrics are essential
- Ensemble models perform better for complex patterns

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook
- GitHub

---

## Key Learning Outcomes

- Handling imbalanced datasets
- Using class_weight for balanced learning
- Applying stratified sampling
- Evaluating models using appropriate metrics
- Building end-to-end classification pipelines

---

## Conclusion

This project demonstrates a real-world application of machine learning in fraud detection. By addressing class imbalance and using appropriate evaluation techniques, the model can effectively identify fraudulent transactions and support financial security systems.
