# Life Expectancy and GDP

An exploratory analysis of the relationship between economic output and life expectancy across six countries from 2000 to 2015.

## 1. Technologies & Concepts

- Python
- pandas
- Matplotlib and Seaborn
- Exploratory data analysis
- Time-series visualization
- Grouped descriptive statistics
- Distribution analysis
- Correlation-oriented visual exploration

## 2. Key Findings

- The dataset contains 96 observations covering Chile, China, Germany, Mexico, the United States, and Zimbabwe over 16 years (2000–2015).
- Life expectancy generally trends upward. Zimbabwe is the main exception early in the period: it declines until 2004 and then rises strongly; the notebook reports an increase of roughly 33% from its lowest point.
- GDP growth is especially pronounced for China and the United States, with Germany also showing growth, while Chile, Mexico, and Zimbabwe show less dramatic changes in the analysis.
- The notebook identifies a positive relationship between GDP and life expectancy for the six countries studied.
- Average life expectancy over the period is highest for Germany (~79.66 years), followed by Chile (~78.94) and the United States (~78.06); Zimbabwe is substantially lower at ~50.09 years.

These findings describe this dataset and time period and should not be interpreted as evidence that GDP alone causes changes in life expectancy.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter pandas matplotlib seaborn
jupyter notebook analysis.ipynb
```

The dataset is included at `data/all_data.csv`.
