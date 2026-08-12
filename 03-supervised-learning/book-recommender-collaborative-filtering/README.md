# Book Recommender with Collaborative Filtering

A prototype recommender system that predicts user ratings with neighborhood-based collaborative filtering.

**Originally developed (first GitHub commit): December 19, 2024 · [View original repository](https://github.com/DavidAlmagro/BookRecommender_SVM_Prototype)**

## 1. Technologies & Concepts

- Python and pandas
- Surprise (`scikit-surprise`)
- Collaborative filtering
- K-nearest-neighbor recommendation (`KNNBasic`)
- User–item rating data
- Train/test splitting
- Root Mean Squared Error (RMSE)
- Point prediction for individual user–book pairs

## 2. Key Findings

- The source data contains 3,500 user–book rating records before filtering invalid zero ratings.
- Ratings of 4 and 5 are the most common valid values in the stored dataset.
- The `KNNBasic` collaborative-filtering model records an RMSE of approximately **1.043** on the held-out test data.
- A stored example prediction estimates a rating of **3.81** for a specific user–book pair.
- Despite the name of the original standalone repository, the implemented model is KNN-based collaborative filtering rather than an SVM; the portfolio folder has therefore been renamed to reflect the actual technique.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter pandas scikit-surprise
jupyter notebook analysis.ipynb
```

The rating data is included at `data/20241208_rating_data.csv`.
