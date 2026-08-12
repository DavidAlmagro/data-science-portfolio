# Data Science Portfolio

A curated collection of data science projects spanning exploratory analysis, statistical reasoning, feature engineering, classical machine learning, unsupervised learning, and neural networks.

The repository consolidates independent learning and portfolio projects into a single, navigable structure. Each project includes its notebook, data where applicable, and a standardized README covering the techniques used, the main findings, and reproducibility.

## Featured Projects

| Project | Area | Highlight |
|---|---|---|
| [Life Expectancy and GDP](01-data-analysis/life-expectancy-gdp/) | Data Analysis | Cross-country EDA of GDP and life expectancy from 2000–2015 |
| [Biodiversity in U.S. National Parks](01-data-analysis/biodiversity-national-parks/) | Data Analysis | Biodiversity, conservation status, and observation patterns across four national parks |
| [Baseball Strike Zones with SVM](03-supervised-learning/baseball-strike-zones-svm/) | Supervised Learning | Non-linear SVM decision boundaries on MLB pitch-location data, reaching ~83% validation accuracy |
| [Income Prediction with Random Forest](03-supervised-learning/income-prediction-random-forest/) | Supervised Learning | Random Forest tuning and feature engineering, improving test accuracy to ~85% |
| [Olivetti Faces with PCA](04-unsupervised-learning/olivetti-faces-pca/) | Unsupervised Learning | Eigenfaces, dimensionality reduction, and reconstruction of 4,096-dimensional face images |
| [Heart Failure Prediction with Deep Learning](05-neural-networks/heart-failure-deep-learning/) | Neural Networks | TensorFlow/Keras classifier with class-level precision/recall analysis |

## Complete Project Matrix

The matrix below shows the **specific techniques**, **input structure and scale**, and a deliberately short **outcome** for every project. For fuller analytical notes and caveats, see [PROJECT_MAP.md](PROJECT_MAP.md).

### 01 — Data Analysis

| Project | Concrete techniques | Inputs | Outcome |
|---|---|---|---|
| [Biodiversity in U.S. National Parks](01-data-analysis/biodiversity-national-parks/) | Data cleaning; EDA; grouped aggregation; categorical analysis; conservation-status analysis; comparative visualization with Matplotlib/Seaborn | 23,296 observation rows + 5,824 species-metadata rows; 5,541 unique species across 4 parks | Yellowstone has the most recorded observations; vascular plants dominate the species catalog. |
| [Diagnosing Diabetes — EDA](01-data-analysis/diagnosing-diabetes/) | Descriptive statistics; hidden-missing-value detection; sentinel-value analysis; dtype validation; categorical-value validation | 768 rows × 9 columns; numeric clinical predictors + binary outcome | Domain-aware validation exposes substantial hidden missingness encoded as zero values. |
| [Life Expectancy and GDP](01-data-analysis/life-expectancy-gdp/) | EDA; time-series visualization; grouped descriptive statistics; distribution analysis; correlation-oriented visual analysis | 96 rows × 4 columns; 6 countries over 16 years (2000–2015) | GDP and life expectancy show a positive association in the six-country sample; correlation is descriptive, not causal. |
| [NBA Trends](01-data-analysis/nba-trends/) | Contingency tables; proportions; chi-square analysis; covariance; Pearson correlation; descriptive statistics; sports visualization | ~24.4k historical NBA rows with mixed categorical/numeric game and forecast variables | Home-court outcome is associated with result; forecast probability and point differential correlate moderately (~0.44). |

### 02 — Feature Engineering

| Project | Concrete techniques | Inputs | Outcome |
|---|---|---|---|
| [Wrapper Feature Selection for Obesity Prediction](02-feature-engineering/wrapper-feature-selection/) | Logistic Regression; Sequential Forward Selection (SFS); Sequential Backward Selection (SBS); Recursive Feature Elimination (RFE); StandardScaler; train/test splitting | 2,111 samples × 18 predictors + outcome; mixed demographic, behavioral, and lifestyle variables | SFS gives the strongest reduced-feature result (~0.783 accuracy) while halving the predictor set. |

### 03 — Supervised Learning

| Project | Concrete techniques | Inputs | Outcome |
|---|---|---|---|
| [Baseball Strike Zones with SVM](03-supervised-learning/baseball-strike-zones-svm/) | `SVC`; RBF/non-linear decision boundaries; train/validation split; `C` and `gamma` tuning; Statcast retrieval with `pybaseball`; spatial decision-boundary visualization | Runtime MLB Statcast pitch data; `plate_x`, `plate_z`, and strike/ball outcome; volume varies by player/date range | Tuned SVM reaches ~83% validation accuracy and learns player-dependent empirical strike-zone boundaries. |
| [Book Recommender with Collaborative Filtering](03-supervised-learning/book-recommender-collaborative-filtering/) | Surprise `KNNBasic`; neighborhood-based collaborative filtering; user–item matrix modeling; 80/20 split; RMSE evaluation; point prediction | 3,500 user–book ratings; 3,380 valid ratings after filtering zeros | Held-out RMSE is ~1.043; the implementation is KNN collaborative filtering, not SVM. |
| [Car Acceptability with Gradient Boosting](03-supervised-learning/car-acceptability-gradient-boosting/) | One-hot encoding; `GradientBoostingClassifier`; 70/30 split; accuracy/precision/recall/F1; confusion-matrix analysis | 1,728 UCI records; 6 categorical predictors + target | Test accuracy is ~89.8% with recall ~0.896 and F1 ~0.839. |
| [Email Similarity with Naive Bayes](03-supervised-learning/email-similarity-naive-bayes/) | `CountVectorizer`; bag-of-words; sparse text representation; `MultinomialNB`; train/test evaluation; repeated category-pair experiments | Runtime 20 Newsgroups text; exact sample count varies with selected categories | Accuracy ranges ~86–99%, showing how vocabulary overlap drives class separability. |
| [Income Prediction with Random Forest](03-supervised-learning/income-prediction-random-forest/) | Categorical encoding; Random Forest; `max_depth` tuning; feature importance; derived `education_bin`; class-imbalance analysis | 32,561 UCI Adult rows; mixed numeric/categorical predictors; imbalanced binary income target | Feature engineering raises best stored test accuracy to ~84.98%. |
| [Raisin Classification](03-supervised-learning/raisin-classification/) | Decision Tree; Logistic Regression; `GridSearchCV`; `RandomizedSearchCV`; cross-validation; hyperparameter search | 900 samples × 7 numeric morphology features; balanced 450/450 classes | Tuned Logistic Regression reaches ~87.08% CV accuracy, outperforming the tuned tree in stored CV results. |
| [Wine Quality with Regularized Logistic Regression](03-supervised-learning/wine-quality-regularization/) | Standardization; Logistic Regression; L1/Lasso; L2/Ridge; `GridSearchCV`; `LogisticRegressionCV`; F1 optimization; coefficient-based feature interpretation | 1,599 red-wine rows × 11 physicochemical predictors + quality; white-wine data retained as supporting input | Regularization demonstrates that better CV scores do not necessarily improve held-out F1. |

### 04 — Unsupervised Learning

| Project | Concrete techniques | Inputs | Outcome |
|---|---|---|---|
| [Handwriting Recognition with K-Means](04-unsupervised-learning/handwriting-recognition-kmeans/) | K-Means; 10-cluster solution; image-vector clustering; centroid visualization; qualitative cluster interpretation | 1,797 samples × 64 pixels from scikit-learn Digits; 8×8 grayscale images | Cluster centroids become recognizable digit-like prototypes without using labels for fitting. |
| [Olivetti Faces with PCA](04-unsupervised-learning/olivetti-faces-pca/) | Feature standardization; PCA; eigenfaces; principal-component projection; explained-variance representation; inverse transform; image reconstruction | 400 grayscale faces × 4,096 pixel features; 64×64 images | Eigenfaces provide a compact basis that reconstructs salient facial structure from a lower-dimensional representation. |
| [Particle Classification with PCA and SVM](04-unsupervised-learning/particle-classification-pca/) | Standardization; covariance-matrix analysis; eigenvalues/eigenvectors; PCA; explained-variance ratio; 2D projection; SVC comparison | ~19,020 observations × 10 numerical telescope features + gamma/hadron class | Two-component PCA reaches ~71.1% SVM accuracy versus ~72.0% using two standardized original features. |

### 05 — Neural Networks

| Project | Concrete techniques | Inputs | Outcome |
|---|---|---|---|
| [Heart Failure Prediction with Deep Learning](05-neural-networks/heart-failure-deep-learning/) | Column preprocessing; standardization; TensorFlow/Keras `Sequential`; dense layers; binary classification; train/test split; classification report; class-specific error analysis | 299 patients × 12 clinical features; 203 no-death / 96 death events | Test accuracy is ~78.3%, but death-event recall is only 0.52, exposing the key class-specific weakness. |
| [Logic Gates with Perceptrons](05-neural-networks/logic-gates-perceptron/) | scikit-learn `Perceptron`; linear decision boundaries; decision-function visualization; binary classification; linear-separability analysis | Synthetic 4-point, 2D truth tables for AND, OR, and XOR | AND/OR reach 100%; XOR remains at 50%, demonstrating the single-layer perceptron limit. |
| [Perceptron from Scratch](05-neural-networks/perceptron-from-scratch/) | Manual weighted sum; step activation; prediction error; iterative weight updates; custom OOP implementation; training to zero error | 4 manually defined 2D points with ±1 labels | The custom perceptron converges on the tiny linearly separable dataset, exposing the learning rule directly. |

## Technical Coverage

Across the portfolio, the projects demonstrate a progression from **data-quality validation and descriptive analysis** through **statistical reasoning, feature selection, classical supervised learning, hyperparameter optimization, unsupervised representation learning, and neural-network fundamentals**.

Key techniques include:

- **Statistical analysis:** descriptive statistics, contingency tables, chi-square analysis, covariance, Pearson correlation.
- **Feature engineering and selection:** SFS, SBS, RFE, derived features, coefficient sparsity with L1 regularization, tree-based feature importance.
- **Supervised learning:** Logistic Regression, SVM/SVC with RBF kernels, Random Forest, Gradient Boosting, Multinomial Naive Bayes, neighborhood-based collaborative filtering.
- **Model selection:** train/test splits, cross-validation, grid search, randomized search, regularization, F1/RMSE/precision/recall analysis.
- **Unsupervised learning:** K-Means, PCA, eigendecomposition, explained variance, eigenfaces, inverse-transform reconstruction.
- **Neural networks:** perceptron learning rules, linear separability, TensorFlow/Keras dense networks, class-level error analysis.
- **Python ecosystem:** pandas, NumPy, SciPy, Matplotlib, Seaborn, scikit-learn, TensorFlow/Keras, Surprise, mlxtend, pybaseball.

## Repository Structure

```text
data-science-portfolio/
├── 01-data-analysis/
├── 02-feature-engineering/
├── 03-supervised-learning/
├── 04-unsupervised-learning/
├── 05-neural-networks/
├── PROJECT_MAP.md
└── README.md
```

Most project folders follow this layout:

```text
project-name/
├── README.md
├── analysis.ipynb
└── data/              # when the project uses local data files
```

## Reproducibility Notes

- Migrated notebooks are preserved with their saved outputs so documented results can be inspected without rerunning code.
- Local datasets are stored under each project's `data/` directory, and notebook paths have been normalized accordingly.
- Some projects use datasets fetched from public services or scikit-learn at runtime and therefore require internet access on first execution.
- The Baseball Strike Zones notebook references a visualization helper that was not present in the original repository; its project README documents the limitation explicitly.
- No project code was executed as part of the migration. Files were copied and inspected statically.

## About the Migration

These projects were originally maintained as separate repositories. Their original repositories remain available as historical records, while this monorepo provides a cleaner portfolio-oriented view of the work.
