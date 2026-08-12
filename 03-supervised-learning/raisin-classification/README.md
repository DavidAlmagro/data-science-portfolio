# Raisin Classification with Hyperparameter Tuning

A balanced binary-classification exercise comparing grid-search tuning of a decision tree with randomized-search tuning of logistic regression.

**Originally developed (first GitHub commit): December 18, 2024 · [View original repository](https://github.com/DavidAlmagro/RaisinClassification_HyperparameterTuning)**

## 1. Technologies & Concepts

- Python and pandas
- scikit-learn Decision Trees
- Logistic Regression
- `GridSearchCV`
- `RandomizedSearchCV`
- Cross-validation
- Hyperparameter search
- SciPy probability distributions

## 2. Key Findings

- The dataset contains **900 samples**, **7 features**, and two perfectly balanced classes with 450 samples each.
- Grid search selects a decision tree with `max_depth=3`, producing approximately **85.42% cross-validation accuracy** and **85.56% test accuracy**.
- Randomized search over logistic-regression regularization identifies an L2 model with `C≈67.20` and approximately **87.08% cross-validation accuracy**.
- In the stored cross-validation results, tuned logistic regression performs better than the best decision-tree configuration, while the project demonstrates two complementary hyperparameter-search strategies.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter pandas scikit-learn scipy
jupyter notebook analysis.ipynb
```

The dataset is included at `data/Raisin_Dataset.csv`.
