# NBA Trends — Statistical Analysis and Visualization

A statistical exploration of NBA team performance, home-court outcomes, and FiveThirtyEight win forecasts.

**Originally developed (first GitHub commit): December 18, 2024 · [View original repository](https://github.com/DavidAlmagro/NBA_Trends_DataVisualization)**

## 1. Technologies & Concepts

- Python
- pandas and NumPy
- SciPy
- Matplotlib and Seaborn
- Descriptive statistics
- Contingency tables and proportions
- Chi-square testing
- Covariance and Pearson correlation
- Sports analytics and visualization

## 2. Key Findings

- The average scoring gap between the Knicks and Nets in the examined data falls from about 9.73 points in 2010 to about 0.45 points in 2014, indicating much closer scoring performance in the later sample.
- Home teams record 120 wins and 105 losses in the analyzed table, while away teams record 92 wins and 133 losses, suggesting an association between game location and result in this sample.
- The chi-square statistic for location versus result is approximately 6.50.
- FiveThirtyEight's forecast probability has a positive covariance with point differential and a Pearson correlation of approximately 0.44, indicating a moderate positive association: teams assigned higher win probabilities tend to have better point differentials.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter pandas numpy scipy matplotlib seaborn
jupyter notebook analysis.ipynb
```

The NBA dataset is included at `data/nba_games.csv`.
