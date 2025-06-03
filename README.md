# CFPB Consumer Complaint Classification  
### NLP and Machine Learning Project

## 📋 Project Overview

This project leverages **natural language processing (NLP)** and **machine learning** to classify consumer complaints submitted to the **Consumer Financial Protection Bureau (CFPB)**. The goal is to automatically categorize complaints based on their textual content, improving response efficiency and enabling early detection of emerging issues.

---

## 🧾 Dataset

- **Source**: [CFPB Public Consumer Complaint Database](https://www.consumerfinance.gov/data-research/consumer-complaints/)
- **Size**: 2M+ rows
- **Key Fields**:
  - `complaint_what_happened`: Consumer’s narrative (free text)
  - `product`: Complaint category (target variable)
  - Other metadata (e.g., date, company, state)

---

## 🔍 Objective

> Classify the product category of each complaint based on the text description using supervised learning.

---

## 🧹 Data Preparation

- Dropped complaints with missing narratives or categories
- Cleaned text:
  - Lowercased
  - Removed special characters and stopwords
- Transformed text using `TfidfVectorizer`
- Stratified `train_test_split` to ensure balanced class distribution

---

## ⚙️ Modeling

### Algorithms Used:
- **Logistic Regression (SGDClassifier)**: Baseline model
- **XGBoost Classifier**: Advanced ensemble method for performance tuning

### Evaluation Metrics:
- Accuracy
- Precision / Recall / F1-Score
- Confusion Matrix
- Classification Report

### Best Model:
- **XGBoost**, with AUC > 0.85 on stratified validation set

---

## 📊 Visualizations

- Bar chart of top complaint categories
- Confusion matrix heatmap for classification performance

---

## 📁 Project Structure

- `Project 2 - CFPB Consumer Complaints Modeling.ipynb`: Full notebook with analysis and model training
- (Optional) `complaints.csv`: Cleaned and prepared dataset

---

## 🚀 Key Insights

- Text alone can accurately predict complaint category
- Common terms like “loan,” “credit,” and “account” dominate most narratives
- Classification errors often happen between closely related categories (e.g., credit card vs. credit reporting)

---

## 🧭 Future Work

- Incorporate pre-trained embeddings (e.g., BERT)
- Use oversampling or class-weighting for rare categories
- Deploy the model via an API or web interface for real-time use

---

## 📌 Note

This project is for educational purposes using publicly available, de-identified data. It does not provide legal or regulatory conclusions.
