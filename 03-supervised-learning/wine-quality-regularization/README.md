# Wine Quality with Regularized Logistic Regression

A binary wine-quality classification project focused on regularization, cross-validation, and feature selection.

## 1. Technologies & Concepts

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- Logistic Regression
- Standardization
- L1 (Lasso) and L2 (Ridge) regularization
- Grid search and cross-validation
- F1 score
- Coefficient-based feature interpretation

## 2. Key Findings

- Wine quality is reframed as a binary task: ratings above 5 are classified as good wine and ratings of 5 or below as bad wine.
- The unregularized model records an F1 score of approximately **0.773 on training data** and **0.727 on test data**; the stored default L2 result is the same on this split.
- Grid search identifies `C≈0.006893` with a cross-validated F1 of approximately **0.755**, but its held-out test F1 is lower at approximately **0.683**.
- L1 cross-validation selects `C≈0.2595` with a mean cross-validated F1 of approximately **0.749** and enables sparse coefficient-based feature selection.
- The gap between cross-validation selection and held-out performance is a useful reminder that tuning does not guarantee improvement on unseen data and that final test evaluation remains essential.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter pandas numpy matplotlib seaborn scikit-learn
jupyter notebook analysis.ipynb
```

The UCI Wine Quality supporting files are stored in `data/`.
