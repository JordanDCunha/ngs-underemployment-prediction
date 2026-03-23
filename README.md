# Graduate Underemployment Prediction (HackML 2026)

## 📌 Overview
This project predicts whether graduates are overqualified for their current jobs using survey data from the National Graduates Survey (NGS 2020).

## 📊 Dataset
- ~7,700 training samples
- 20+ categorical and ordinal features
- Includes education, demographics, financial, and work experience data

## 🧠 Approach

### Data Cleaning
- Handled special survey codes (6, 9, 97, 99) as missing values
- Created missing value indicators

### Feature Engineering
- Education progression (`CERTLEVP - PREVLEVP`)
- Financial pressure (`debt - scholarships`)
- Parent education advantage
- Log-transformed work experience
- Interaction features (age × education)

### Modeling
- CatBoost classifier (native categorical handling)
- Stratified 5-fold cross-validation
- Multiple ensemble strategies:
  - Baseline averaging
  - Filtered folds (high-performing splits)
  - Weighted ensemble

## 📈 Results
- Cross-validation ROC AUC: ~0.70+
- Competitive with top leaderboard scores (~0.71)

## 🧪 Key Learnings
- Proper handling of categorical data significantly improves performance
- Feature quality matters more than model complexity
- Cross-validation helps reduce variance and improve generalization
- Not all folds contribute equally in ensemble models

## 🚀 How to Run

```bash
pip install catboost pandas numpy scikit-learn

## Graduate Underemployment Prediction (HackML 2026)

🔗 Competition Page: https://www.kaggle.com/competitions/ng-hackml-2026/overview
