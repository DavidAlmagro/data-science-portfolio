# Heart Failure Prediction with Deep Learning

A TensorFlow/Keras binary-classification project using clinical records to predict heart-failure mortality outcomes.

## 1. Technologies & Concepts

- Python
- pandas and NumPy
- scikit-learn preprocessing and train/test splitting
- TensorFlow / Keras `Sequential` models
- Dense neural networks
- Feature standardization and categorical handling
- Binary classification
- Precision, recall, F1 score, and classification reports
- Class-imbalance and error analysis

## 2. Key Findings

- The dataset contains **299 patients**: 203 without a recorded death event and 96 with a death event.
- The stored split contains 239 training observations and 60 test observations across 12 clinical features.
- The neural network achieves approximately **78.3% test accuracy**.
- For patients without a death event, the stored report shows precision **0.74**, recall **0.97**, and F1 **0.84**.
- For patients with a death event, precision is high at **0.93**, but recall is only **0.52**, with F1 **0.67**.
- The lower recall for the death-event class is the most important limitation: despite reasonable overall accuracy, the model misses a substantial share of true high-risk cases. In a clinical setting, that trade-off would require careful attention before any practical use.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter pandas numpy scikit-learn tensorflow
jupyter notebook analysis.ipynb
```

The clinical dataset is included in `data/`.
