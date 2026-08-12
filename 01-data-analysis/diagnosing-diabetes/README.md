# Diagnosing Diabetes — Exploratory Data Analysis

A compact data-quality and exploratory-analysis exercise using a diabetes dataset.

**Originally developed (first GitHub commit): December 18, 2024 · [View original repository](https://github.com/DavidAlmagro/DiagnosingDiabetes_EDA)**

## 1. Technologies & Concepts

- Python
- pandas and NumPy
- Exploratory data analysis (EDA)
- Summary statistics
- Missing-data detection
- Data-type and categorical-value validation
- Data-quality diagnostics

## 2. Key Findings

- The dataset contains 768 observations and nine columns.
- A conventional null-value check initially reports no missing values, but summary statistics expose implausible zero values in medically meaningful fields.
- Interpreting those zeros as missing-value sentinels reveals 5 affected glucose records, 35 blood-pressure records, 227 skin-thickness records, 374 insulin records, and 11 BMI records.
- The target column also contains an unexpected `O` value alongside `0` and `1`, demonstrating why categorical validation matters even when data types appear valid.
- The central lesson is that data quality cannot be assessed with `isna()` alone; domain-aware inspection and descriptive statistics can uncover hidden issues.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter pandas numpy
jupyter notebook analysis.ipynb
```

Run the command from this folder. The dataset is included at `data/diabetes.csv`.
