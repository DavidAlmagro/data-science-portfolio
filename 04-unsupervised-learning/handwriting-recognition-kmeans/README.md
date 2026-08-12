# Handwriting Recognition with K-Means

An unsupervised-learning exercise that explores whether K-Means cluster centers can recover digit-like prototypes from handwritten images.

## 1. Technologies & Concepts

- Python and NumPy
- Matplotlib
- scikit-learn datasets
- K-Means clustering
- Unsupervised learning
- Image vectors and cluster centroids
- Visual interpretation of learned prototypes

## 2. Key Findings

- The scikit-learn Digits dataset contains **1,797 samples** represented by **64 pixel features** (8×8 images).
- K-Means is configured with **10 clusters**, matching the ten digit classes without using labels during clustering.
- Visualizing the ten cluster centers produces digit-like centroid images, demonstrating that meaningful structure can emerge from pixel data through unsupervised grouping.
- The notebook focuses on qualitative cluster interpretation rather than reporting a formal classification-accuracy metric, so the result should be understood as a clustering demonstration rather than a supervised handwriting classifier benchmark.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter numpy matplotlib scikit-learn
jupyter notebook analysis.ipynb
```

The Digits dataset is bundled with scikit-learn, so no separate local data file is required.
