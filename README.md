# Data Science Portfolio

A curated collection of data science projects spanning exploratory analysis, statistical reasoning, feature engineering, classical machine learning, unsupervised learning, and neural networks.

The repository consolidates a set of independent learning and portfolio projects into a single, navigable structure. Each project keeps its notebook and data together and includes a standardized README focused on the techniques used, the findings produced, and reproducibility.

## Featured Projects

| Project | Area | Highlights |
|---|---|---|
| [Life Expectancy and GDP](01-data-analysis/life-expectancy-gdp/) | Data Analysis | Cross-country EDA and visualization of GDP and life expectancy from 2000–2015 |
| [Biodiversity in U.S. National Parks](01-data-analysis/biodiversity-national-parks/) | Data Analysis | Biodiversity, conservation status, and observation patterns across four national parks |
| [Baseball Strike Zones with SVM](03-supervised-learning/baseball-strike-zones-svm/) | Supervised Learning | SVM decision boundaries on MLB pitch-location data, with ~83% validation accuracy after tuning |
| [Income Prediction with Random Forest](03-supervised-learning/income-prediction-random-forest/) | Supervised Learning | Random Forest tuning and feature engineering, improving test accuracy from ~83.5% to ~85.0% |
| [Olivetti Faces with PCA](04-unsupervised-learning/olivetti-faces-pca/) | Unsupervised Learning | Eigenfaces, dimensionality reduction, and reconstruction of 4,096-dimensional face images |
| [Heart Failure Prediction with Deep Learning](05-neural-networks/heart-failure-deep-learning/) | Neural Networks | TensorFlow/Keras binary classifier with 78% test accuracy and class-level error analysis |

## Project Map

For a portfolio-wide comparison of the **concrete techniques, input data/volume, and stored outcomes for all 18 projects**, see the [Complete Project Techniques, Inputs, and Outcomes Map](PROJECT_MAP.md).

### 01 — Data Analysis

- [Biodiversity in U.S. National Parks](01-data-analysis/biodiversity-national-parks/)
- [Diagnosing Diabetes — Exploratory Data Analysis](01-data-analysis/diagnosing-diabetes/)
- [Life Expectancy and GDP](01-data-analysis/life-expectancy-gdp/)
- [NBA Trends — Statistical Analysis and Visualization](01-data-analysis/nba-trends/)

### 02 — Feature Engineering

- [Wrapper Feature Selection for Obesity Prediction](02-feature-engineering/wrapper-feature-selection/)

### 03 — Supervised Learning

- [Baseball Strike Zones with Support Vector Machines](03-supervised-learning/baseball-strike-zones-svm/)
- [Book Recommender with Collaborative Filtering](03-supervised-learning/book-recommender-collaborative-filtering/)
- [Car Acceptability with Gradient Boosting](03-supervised-learning/car-acceptability-gradient-boosting/)
- [Email Similarity with Naive Bayes](03-supervised-learning/email-similarity-naive-bayes/)
- [Income Prediction with Random Forest](03-supervised-learning/income-prediction-random-forest/)
- [Raisin Classification with Hyperparameter Tuning](03-supervised-learning/raisin-classification/)
- [Wine Quality with Regularized Logistic Regression](03-supervised-learning/wine-quality-regularization/)

### 04 — Unsupervised Learning

- [Handwriting Recognition with K-Means](04-unsupervised-learning/handwriting-recognition-kmeans/)
- [Olivetti Faces with PCA](04-unsupervised-learning/olivetti-faces-pca/)
- [Particle Classification with PCA and SVM](04-unsupervised-learning/particle-classification-pca/)

### 05 — Neural Networks

- [Heart Failure Prediction with Deep Learning](05-neural-networks/heart-failure-deep-learning/)
- [Logic Gates with Perceptrons](05-neural-networks/logic-gates-perceptron/)
- [Perceptron from Scratch](05-neural-networks/perceptron-from-scratch/)

## Skills Matrix

| Area | Concepts demonstrated |
|---|---|
| Data analysis | Data cleaning, exploratory data analysis, descriptive statistics, hypothesis-oriented exploration, visualization |
| Statistical reasoning | Correlation, covariance, contingency tables, chi-square analysis |
| Feature engineering | Wrapper methods, sequential feature selection, recursive feature elimination, derived features |
| Supervised learning | Logistic regression, SVM, Random Forest, Gradient Boosting, Naive Bayes, collaborative filtering |
| Model selection | Train/test splits, cross-validation, grid search, randomized search, regularization, metric comparison |
| Unsupervised learning | K-Means, PCA, dimensionality reduction, eigenfaces |
| Neural networks | Perceptrons, linear separability, TensorFlow/Keras dense networks |
| Python ecosystem | pandas, NumPy, Matplotlib, Seaborn, SciPy, scikit-learn, TensorFlow/Keras, Surprise, pybaseball |

## Repository Structure

```text
data-science-portfolio/
├── 01-data-analysis/
├── 02-feature-engineering/
├── 03-supervised-learning/
├── 04-unsupervised-learning/
├── 05-neural-networks/
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

- Migrated notebooks are preserved with their saved outputs so the documented results can be inspected without rerunning code.
- Local datasets are stored under each project's `data/` directory, and notebook paths have been normalized accordingly.
- Some projects use datasets fetched from public services or scikit-learn at runtime and therefore require internet access on first execution.
- The Baseball Strike Zones notebook references a visualization helper that was not present in the original repository; its README documents the limitation explicitly.
- No project code was executed as part of the migration. Files were copied and inspected statically.

## About the Migration

These projects were originally maintained as separate repositories. Their original repositories remain available as historical records, while this monorepo provides a cleaner portfolio-oriented view of the work.
