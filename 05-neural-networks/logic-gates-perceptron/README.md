# Logic Gates with Perceptrons

A visual introduction to linear separability through perceptron models of AND, OR, and XOR logic gates.

## 1. Technologies & Concepts

- Python and NumPy
- scikit-learn `Perceptron`
- Matplotlib
- Binary classification
- Linear decision boundaries
- Linear separability
- Decision-function visualization
- Fundamental neural-network limitations

## 2. Key Findings

- A single perceptron learns the **AND** gate with **100% accuracy**.
- It also learns the **OR** gate with **100% accuracy**.
- The same linear model reaches only **50% accuracy** on **XOR** in the stored experiment.
- AND and OR are linearly separable, so one straight decision boundary is sufficient.
- XOR is not linearly separable, which exposes the fundamental limitation of a single-layer perceptron and motivates multilayer/non-linear neural-network architectures.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter numpy matplotlib scikit-learn
jupyter notebook analysis.ipynb
```

No external dataset is required; the logic-gate truth tables are defined directly in the notebook.
