# Olivetti Faces with PCA

A dimensionality-reduction project demonstrating eigenfaces, compression, and reconstruction on grayscale face images.

**Originally developed (first GitHub commit): December 18, 2024 · [View original repository](https://github.com/DavidAlmagro/OlivettiFaces_PCA)**

## 1. Technologies & Concepts

- Python
- NumPy and pandas
- Matplotlib
- scikit-learn PCA
- Data standardization
- Principal Component Analysis
- Eigenfaces
- Dimensionality reduction and inverse transformation
- Image reconstruction

## 2. Key Findings

- Each Olivetti face is represented by **4,096 pixel features**, corresponding to a 64×64 grayscale image.
- PCA is fitted with up to **400 principal components**, transforming the standardized high-dimensional face vectors into a lower-dimensional representation.
- The notebook visualizes learned eigenfaces and reconstructs images through the PCA inverse transform, demonstrating how a basis of principal components can represent salient facial structure.
- No reconstruction-error metric is stored, so the project emphasizes visual and conceptual understanding of compression rather than claiming a quantified optimal compression ratio.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter numpy pandas matplotlib scikit-learn
jupyter notebook analysis.ipynb
```

The notebook uses scikit-learn's Olivetti Faces loader. The dataset may be downloaded automatically on first use, so internet access can be required.
