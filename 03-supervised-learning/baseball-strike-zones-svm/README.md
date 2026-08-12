# Baseball Strike Zones with Support Vector Machines

An SVM-based analysis of called strike zones using MLB pitch-location data for Aaron Judge, Jose Altuve, and David Ortiz.

## 1. Technologies & Concepts

- Python
- scikit-learn Support Vector Classification (`SVC`)
- `pybaseball` and Statcast data
- NumPy and Matplotlib
- Train/validation splitting
- Non-linear decision boundaries
- Hyperparameter exploration (`C` and `gamma`)
- Sports analytics and spatial visualization

## 2. Key Findings

- A baseline SVM classifier achieves approximately 82.82% validation accuracy in the stored notebook results.
- Exploring combinations of `C` and `gamma` produces configurations around 83% validation accuracy, showing a modest improvement over the baseline.
- The project demonstrates how pitch location (`plate_x` and `plate_z`) can be used to model empirical strike/ball decision boundaries rather than relying only on the rulebook strike zone.
- Comparing players with very different physical builds illustrates why learned strike-zone boundaries can vary between batters.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter numpy matplotlib scikit-learn pybaseball pandas
jupyter notebook analysis.ipynb
```

Internet access is required when `pybaseball` retrieves Statcast data.

**Reproducibility note:** the original repository references a local helper module named `svm_visualization.py` for `draw_boundary`, but that file was not present in the original source. The data-processing and model-training sections are preserved; reproducing the custom boundary plots requires supplying an equivalent helper or replacing those calls with a Matplotlib contour visualization of the SVM decision function.
