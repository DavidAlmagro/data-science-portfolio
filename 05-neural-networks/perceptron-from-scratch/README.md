# Perceptron from Scratch

A minimal implementation of a perceptron class designed to expose the mechanics that machine-learning libraries normally abstract away.

## 1. Technologies & Concepts

- Python
- Object-oriented programming
- Perceptron architecture
- Weighted sums and activation functions
- Prediction error
- Iterative weight updates
- Learning-rate and training-loop concepts
- Neural-network fundamentals without a machine-learning framework

## 2. Key Findings

- The project implements the core perceptron workflow manually: calculate a weighted sum, apply an activation function, compare the prediction with the target, and update the weights from the resulting error.
- The notebook is primarily an educational implementation rather than a benchmarked predictive model; it does not store a formal accuracy or loss metric.
- Building the algorithm without scikit-learn makes the relationship between inputs, weights, activation, error, and learning behavior explicit.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter
jupyter notebook analysis.ipynb
```

No external dataset or third-party machine-learning library is required by the notebook implementation.
