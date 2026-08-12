# Car Acceptability with Gradient Boosting

A binary classification project that predicts whether a car is acceptable from price and technical attributes.

## 1. Technologies & Concepts

- Python
- pandas and NumPy
- scikit-learn `GradientBoostingClassifier`
- Categorical one-hot encoding
- Train/test splitting
- Accuracy, precision, recall, and F1 score
- Confusion-matrix analysis
- Ensemble learning and gradient boosting

## 2. Key Findings

- A Gradient Boosting classifier with 15 estimators achieves approximately **89.8% test accuracy**.
- The stored test metrics are approximately **0.789 precision**, **0.896 recall**, and **0.839 F1** for the positive class.
- The confusion matrix records 138 true positives, 16 false negatives, 37 false positives, and 328 true negatives.
- The results show strong overall classification performance while also illustrating why multiple metrics are more informative than accuracy alone.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter pandas numpy scikit-learn
jupyter notebook analysis.ipynb
```

The notebook downloads the UCI Car Evaluation dataset directly from the UCI Machine Learning Repository, so internet access is required when the data-loading cell is executed.
