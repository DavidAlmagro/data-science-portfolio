# Income Prediction with Random Forest

A Random Forest classification project using census data to predict whether income exceeds $50K, including hyperparameter tuning and feature engineering.

## 1. Technologies & Concepts

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- scikit-learn Random Forests and decision trees
- Categorical feature encoding
- Train/test splitting
- Hyperparameter tuning with tree depth
- Feature importance
- Feature engineering
- Class imbalance awareness

## 2. Key Findings

- The target is imbalanced: approximately **75.92%** of observations are in the `<=50K` class and **24.08%** in the `>50K` class.
- The baseline Random Forest records about **82% accuracy**.
- Tuning `max_depth` raises the best stored test accuracy to approximately **83.46%** at depth 12.
- The five most important stored features are `capital-gain`, `age`, `hours-per-week`, `capital-loss`, and `sex_Male`.
- Adding an engineered `education_bin` feature improves the best stored test accuracy to approximately **84.98%** at depth 14.
- Because of the class imbalance, the notebook correctly notes that future tuning against F1 or ROC-AUC could reveal different model trade-offs than optimizing accuracy alone.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter pandas numpy matplotlib seaborn scikit-learn
jupyter notebook analysis.ipynb
```

The census data is included at `data/adult.data`.
