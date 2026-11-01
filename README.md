# Phishing Detection System
Detects phishing URLs using machine learning.

## Status: In Progress 🚧

## Plan
- [x] Collect dataset
- [x] Select URL-based features
- [ ] Train and compare models
- [ ] Build Streamlit app

## Dataset
PhiUSIIL Phishing URL Dataset (Kaggle): 235,795 URLs, 55 columns.
label 1 = legitimate (134,850), label 0 = phishing (100,945).
Train/test split: 80/20 (stratified).

## Results

| Model | Features | Accuracy | Precision | Recall |
|---|---|---|---|---|
| Random Forest | All 50 numeric features | 100% | 100% | 100% |
| Random Forest | URL-only (21 features) | 99.66% | 99.56% | 99.84% |

Note: the 100% result uses page-content features (e.g. LineOfCode,
NoOfExternalRef) that need the page to be fetched, so it is not realistic
for a URL-only app. The URL-only model is the one used in this project.
