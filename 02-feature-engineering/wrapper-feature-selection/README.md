# Wrapper Feature Selection for Obesity Prediction

A comparison of wrapper-based feature-selection strategies applied to logistic-regression obesity prediction.

## 1. Technologies & Concepts

- Python and pandas
- scikit-learn Logistic Regression
- mlxtend Sequential Feature Selector
- Sequential Forward Selection (SFS)
- Sequential Backward Selection (SBS)
- Recursive Feature Elimination (RFE)
- Feature scaling with `StandardScaler`
- Train/test splitting and model accuracy

## 2. Key Findings

- The modeling dataset contains 2,111 samples and 18 predictor variables.
- Sequential Forward Selection reduces the model to nine features and produces an average accuracy of approximately 0.783 in the stored result.
- Sequential Backward Selection uses seven features and produces approximately 0.764 accuracy.
- Recursive Feature Elimination also selects seven features and records an accuracy of approximately 0.763.
- Among the tested reduced subsets, SFS provides the strongest stored result while still cutting the original 18 predictors in half.
- Age, family history of overweight, frequent high-calorie-food consumption (`FAVC`), and eating-between-meals behavior (`CAEC`) recur across multiple selected subsets, suggesting they are consistently useful predictors in this exercise.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter pandas scikit-learn mlxtend matplotlib
jupyter notebook analysis.ipynb
```

The survey data is included at `data/obesity.csv`.
