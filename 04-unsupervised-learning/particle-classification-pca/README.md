# Particle Classification with PCA and SVM

A dimensionality-reduction and classification project exploring gamma-versus-hadron telescope data with PCA and Support Vector Machines.

## 1. Technologies & Concepts

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- scikit-learn PCA
- Support Vector Classification (`SVC`)
- Matrix standardization
- Eigenvalues, eigenvectors, and explained variance
- Two-dimensional projection
- Train/test evaluation

## 2. Key Findings

- The leading principal component explains approximately **28.85%** of the variance in the stored PCA result.
- An SVM trained on a two-component PCA representation achieves approximately **71.06% accuracy** on the stored test split.
- An SVM using the first two standardized original features achieves approximately **72.00% accuracy** on the corresponding comparison split.
- In this experiment, the two-dimensional PCA representation remains competitive but does not outperform the selected pair of original standardized features.
- The project demonstrates the trade-off between dimensionality reduction, visual interpretability, and downstream predictive performance.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter pandas numpy matplotlib seaborn scikit-learn
jupyter notebook analysis.ipynb
```

The source datasets and supporting matrices are included in `data/`.
