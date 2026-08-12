# Temporary Notebook Static Analysis

Generated without executing notebook code. Only stored source text and saved outputs are inspected.

## 01-data-analysis/biodiversity-national-parks

### Imports
- `from matplotlib import pyplot as plt`
- `import numpy as np`
- `import pandas as pd`
- `import seaborn as sns`

### Headings
- # Introduction
- ## Data sources:
- # Import Python Modules
- # Data Acquisition & Preparation
- ## Data Import
- ### *observations.csv*
- ### *species_info.csv*
- ## Data Exploration & Cleaning
- # Analysis & Interpretation: Data Visualization and Hypothesis Testing
- ## Species Observations
- ## Species Information
- # Conclusions

### Result-oriented markdown
- # Introduction This project aims to analyze biodiversity within four prominent national parks in the United States: Bryce Canyon, Great Smoky Mountains, Yellowstone, and Yosemite. Using Python, we will explore species observations, conservation statuses, and their ecological implications. The analysis will address the following key questions: **1. Species Observations** - *Most Observed Species*: Identify the species that are most frequently observed in each park to understand which are better adapted to these environments. - *Variability Across Parks*: Compare species observations across the four parks to reveal significant patterns and differences in biodiversity. - *Temporal Trends*: Analyze historical observation data to determine trends over time, including whether certain species sightings are increasing or decreasing. **2. Species Information** - *Species Distribution by Category*: Examine the distribution of species across categories (Amphibian, Bird, etc.) to understand which groups are most represented in each park. - *Conservation Status*: Identify species with endangered statuses and assess how these species are distributed across the parks, providing insight into conse
- # Data Acquisition & Preparation ## Data Import ### *observations.csv* This dataset contains records of species observations across four national parks. The fields are as follows: - **scientific_name**: The scientific name of the species observed, following the binomial nomenclature system. - **park_name**: The name of the national park where the observation was made. The parks included are Bryce Canyon, Great Smoky Mountains, Yellowstone, and Yosemite. - **observations**: The number of times each species has been observed in the respective park, providing insights into species abundance and distribution.
- ### *species_info.csv* This dataset provides detailed information about various species, including their classification and conservation status. The fields are as follows: - **category**: The taxonomic category of the species, which can include Amphibian, Bird, Fish, Mammal, Nonvascular Plant, Reptile, or Vascular Plant. - **scientific_name**: The scientific name of the species, which matches the names in the observations dataset for easy cross-referencing. - **common_names**: Common names or vernacular names associated with the species, providing a more relatable reference for non-scientific audiences. - **conservation_status**: The conservation status of the species, which may be empty or indicate statuses such as Endangered, In Recovery, Species of Concern, or Threatened, highlighting the species' risk levels.
- ## Data Exploration & Cleaning **observations.csv**
- # Analysis & Interpretation: Data Visualization and Hypothesis Testing ## Species Observations **Most Observed species in each park**
- **Comparison of species (categories) observations across parks: patterns and differences in biodiversity**
- # Conclusions

### Metric/result code
- None found

### Saved textual outputs
- scientific_name park_name observations 0 Vicia benghalensis Great Smoky Mountains National Park 68 1 Neovison vison Great Smoky Mountains National Park 77 2 Prunus subcordata Yosemite National Park 138 3 Abutilon theophrasti Bryce National Park 84 4 Githopsis specularioides Great Smoky Mountains National Park 85
- <class 'pandas.core.frame.DataFrame'> RangeIndex: 23296 entries, 0 to 23295 Data columns (total 3 columns): # Column Non-Null Count Dtype --- ------ -------------- ----- 0 scientific_name 23296 non-null string 1 park_name 23296 non-null string 2 observations 23296 non-null int64 dtypes: int64(1), string(2) memory usage: 546.1 KB
- # of Unique values for scientific_name: 5541 # of Unique values for park_name: 4 Range of values for observations: [9, 321]
- park_name Bryce National Park 5541 Great Smoky Mountains National Park 5541 Yellowstone National Park 5541 Yosemite National Park 5541 Name: scientific_name, dtype: int64
- park_name Bryce National Park 576025 Great Smoky Mountains National Park 431820 Yellowstone National Park 1443562 Yosemite National Park 863332 Name: observations, dtype: int64
- <class 'pandas.core.frame.DataFrame'> RangeIndex: 5824 entries, 0 to 5823 Data columns (total 4 columns): # Column Non-Null Count Dtype --- ------ -------------- ----- 0 category 5824 non-null category 1 scientific_name 5824 non-null string 2 common_names 5824 non-null string 3 conservation_status 5824 non-null category dtypes: category(2), string(2) memory usage: 103.1 KB
- # of Unique values for category: 7 # of Unique values for scientific_name: 5541 # of Unique values for common_names: 5504 # of Unique values for conservation_status: 5
- Conservation status: ['No Intervention', 'Species of Concern', 'Endangered', 'Threatened', 'In Recovery'] Categories (5, object): ['No Intervention' < 'Species of Concern' < 'In Recovery' < 'Threatened' < 'Endangered'] ['No Intervention', 'Species of Concern', 'Endangered', 'Threatened', 'In Recovery'] Categories (5, object): ['No Intervention' < 'Species of Concern' < 'In Recovery' < 'Threatened' < 'Endangered']
- category Vascular Plant 4262 Bird 488 Nonvascular Plant 333 Mammal 176 Fish 125 Amphibian 79 Reptile 78 Name: scientific_name, dtype: int64
- <Figure size 1200x800 with 1 Axes>
- <Figure size 1200x800 with 0 Axes>
- <Figure size 640x480 with 1 Axes>

---

## 01-data-analysis/diagnosing-diabetes

### Imports
- `import pandas as pd`
- `import numpy as np`

### Headings
- # EDA: Diagnosing Diabetes
- ## Initial Inspection
- ## Further Inspection
- # Next Steps:

### Result-oriented markdown
- 4. How many rows (observations) does the data contain?
- 6. If you answered no to the question above, not so fast! While it's technically true that none of the columns contain null values, that doesn't necessarily mean that the data isn't missing any values. When exploring data, you should always question your assumptions and try to dig deeper. To investigate further, calculate summary statistics on `diabetes_data` using the `.describe()` method.
- 7. Looking at the summary statistics, do you notice anything odd about the following columns? - `Glucose` - `BloodPressure` - `SkinThickness` - `Insulin` - `BMI`
- 13. Next, take a closer look at the data types of each column in `diabetes_data`. Does the result match what you would expect?

### Metric/result code
- `- Instead of changing the `0` values in the five columns to `NaN`, try replacing the values with the median or mean of each column.`

### Saved textual outputs
- 9
- 768
- Pregnancies 0 Glucose 0 BloodPressure 0 SkinThickness 0 Insulin 0 BMI 0 DiabetesPedigreeFunction 0 Age 0 Outcome 0 dtype: int64
- Pregnancies Glucose BloodPressure SkinThickness Insulin \ count 768.000000 768.000000 768.000000 768.000000 768.000000 mean 3.845052 120.894531 69.105469 20.536458 79.799479 std 3.369578 31.972618 19.355807 15.952218 115.244002 min 0.000000 0.000000 0.000000 0.000000 0.000000 25% 1.000000 99.000000 62.000000 0.000000 0.000000 50% 3.000000 117.000000 72.000000 23.000000 30.500000 75% 6.000000 140.250000 80.000000 32.000000 127.250000 max 17.000000 199.000000 122.000000 99.000000 846.000000 BMI DiabetesPedigreeFunction Age count 768.000000 768.000000 768.000000 mean 31.992578 0.471876 33.240885 std 7.884160 0.331329 11.760232 min 0.000000 0.078000 21.000000 25% 27.300000
- Pregnancies 0 Glucose 5 BloodPressure 35 SkinThickness 227 Insulin 374 BMI 11 DiabetesPedigreeFunction 0 Age 0 Outcome 0 dtype: int64
- ['1' '0' 'O']

---

## 01-data-analysis/life-expectancy-gdp

### Imports
- `from matplotlib import pyplot as plt`
- `import pandas as pd`
- `import seaborn as sns`

### Headings
- # Introduction
- # Import Python Modules
- # Import the data
- # Data Exploration
- ## Columns names standarisation
- ## Exploratory plots
- ### GDP distribution
- ## Pairplot: GDP (USD) and Life Expectancy (Yrs)
- #### Deep dive into GDP values
- ##### GDP boxplot
- ##### GDP Line Chart
- #### Deep dive into Life Expectancy values
- ##### Life Expectancy Box Plots
- ##### Life Expectancy Line Charts
- # Conclusions

### Result-oriented markdown
- # Introduction This project aims to investigate the relationship between the economic output of a country and the life expectancy of its citizens. The analysis will focus on identifying significant correlations between GDP and life expectancy across six selected nations. The objectives of this project include data preparation, exploratory data analysis, and visualization of the findings. Specifically, we will seek to answer the following questions: + Has life expectancy shown a positive trend over time in the six selected nations? + Has GDP experienced growth over time in these countries? + Is there a discernible correlation between GDP and life expectancy in each nation? + What is the average life expectancy across these countries? + How is life expectancy distributed among the nations studied? By addressing these questions, we aim to provide insights into the factors that may influence life expectancy and the role of economic performance in public health outcomes. **Data Sources** - GDP Data Source: [World Bank](https://data.worldbank.org/indicator/NY.GDP.MKTP.CD) national accounts data and OECD National Accounts data files. - Life Expectancy Data Source: [World Health Organizati
- Given the previous results, it could be interesting to deep dive into the evolution of GDP over time. Due to the boxes sizes, we could expect China and USA to have experienced the biggest changes over the years
- We can observe a consistent upward trend with a similar slope for all countries, except for Zimbabwe, which recorded its lowest point in 2004. In that year, its life expectancy began to rise almost exponentially
- # Conclusions In this project, we analyzed a dataset consisting of 96 rows, containing data on GDP and life expectancy for six countries: Chile, China, Germany, Mexico, the United States of America, and Zimbabwe, over a period of 16 years (from 2000 to 2015). The dataset includes four columns, namely 'Country', 'Year', 'Life Expectancy at Birth (Years)', and 'GDP in USD'. In an attempt to answer the initial questions set as the objectives of the project: - Has life expectancy shown a positive trend over time in the six selected nations? Yes, with the exception of Zimbabwe, whose life expectancy curve exhibited a declining slope until 2004, after which it experienced exponential growth, increasing by 33% from its lowest point. - Has GDP experienced growth over time in these countries? This is true for Germany, the United States, and China, with the latter two showing particularly notable growth. However, countries like Chile, Mexico, and Zimbabwe do not exhibit significant growth. - Is there a discernible correlation between GDP and life expectancy in each nation? Yes, there is a positive correlation between GDP and life expectancy for the countries in our list. - What is the averag

### Metric/result code
- `dfMeans = df.drop("Year", axis = 1).groupby("Country").mean().reset_index()`
- `print(dfMeans)`

### Saved textual outputs
- Country Year Life expectancy at birth (years) GDP 0 Chile 2000 77.3 7.786093e+10 1 Chile 2001 77.3 7.097992e+10 2 Chile 2002 77.8 6.973681e+10 3 Chile 2003 77.9 7.564346e+10 4 Chile 2004 78.0 9.921039e+10
- (96, 4)
- ['Chile' 'China' 'Germany' 'Mexico' 'United States of America' 'Zimbabwe']
- [2000 2001 2002 2003 2004 2005 2006 2007 2008 2009 2010 2011 2012 2013 2014 2015]
- Country Year LEAB_Y GDP 0 Chile 2000 77.3 7.786093e+10 1 Chile 2001 77.3 7.097992e+10 2 Chile 2002 77.8 6.973681e+10 3 Chile 2003 77.9 7.564346e+10 4 Chile 2004 78.0 9.921039e+10
- <Figure size 800x600 with 1 Axes>
- /Users/Z004EYJD/anaconda3/lib/python3.11/site-packages/seaborn/axisgrid.py:118: UserWarning: The figure layout has changed to tight self._figure.tight_layout(*args, **kwargs)
- <Figure size 500x500 with 1 Axes>
- <Figure size 500x500 with 6 Axes>
- Country LEAB_Y GDP 0 Chile 78.94375 1.697888e+11 1 China 74.26250 4.957714e+12 2 Germany 79.65625 3.094776e+12 3 Mexico 75.71875 9.766506e+11 4 United States of America 78.06250 1.407500e+13 5 Zimbabwe 50.09375 9.062580e+09
- <Figure size 1400x800 with 1 Axes>
- <Figure size 1200x600 with 1 Axes>

---

## 01-data-analysis/nba-trends

### Imports
- `import pandas as pd`
- `import numpy as np`
- `from scipy.stats import pearsonr, chi2_contingency`
- `import matplotlib.pyplot as plt`
- `import seaborn as sns`

### Headings
- # Codecademy [NBA Trends Project](https://www.codecademy.com/projects/practice/nba-trends)
- ### Task 1
- ### Task 2
- ### Task 3
- ### Task 4
- ### Task 5
- ### Task 6
- ### Task 7
- ### Task 8
- ### Task 9
- ### Task 10
- ### Task 11

### Result-oriented markdown
- ### Task 2 Calculate the difference between the two teams’ average points scored and save the result as diff_means_2010. Based on this value, do you think fran_id and pts are associated? Why or why not?
- ### Task 6 We'd like to know if teams tend to win more games at home compared to away. The variable, `game_result`, indicates whether a team won a particular game ('W' stands for “win” and 'L' stands for “loss”). The variable, `game_location`, indicates whether a team was playing at home or away ('H' stands for “home” and 'A' stands for “away”). Data scientists will often calculate a contingency table of frequencies to help them determine if categorical variables are associated. Calculate a table of frequencies that shows the counts of game_result and game_location. Save your result as `location_result_freq` and print your result. Based on this table, do you think the variables are associated?`
- ### Task 7 Convert this table of frequencies to a table of proportions and save the result as `location_result_proportions`.
- ### Task 9 For each game, 538 has calculated the probability that each team will win the game. We want to know if teams with a higher probability of winning (according to 538) also tend to win games by more points. In the data, 538's prediction is saved as `forecast`. The `point_diff` column gives the margin of victory/defeat for each team (positive values mean that the team won; negative values mean that they lost). Using `nba_2010`, calculate the covariance between `forecast` (538's projected win probability) and `point_diff` (the margin of victory/defeat) in the dataset. Save and print your result. Looking at the matrix, what is the covariance between these two variables?
- ### Task 10 Because 538’s forecast variable is reported as a probability (not a binary), we can calculate the strength of the correlation. Using nba_2010, calculate the correlation between `forecast` and `point_diff`. Call this `point_diff_forecast_corr`. Save and print your result. Does this value suggest an association between the two variables?

### Metric/result code
- `np.set_printoptions(suppress=True, precision = 2)`
- `diff_means_2010 = knicks_pts_10.pts.mean() - nets_pts_10.pts.mean()`
- `print(diff_means_2010)`
- `diff_means_2014 = knicks_pts_14.pts.mean() - nets_pts_14.pts.mean()`
- `print(diff_means_2014)`

### Saved textual outputs
- 9.731707317073173
- <Figure size 640x480 with 1 Axes>
- 0.44706798131809933
- <Figure size 640x480 with 0 Axes>
- game_location A H game_result L 133 105 W 92 120
- game_location A H game_result L 0.295556 0.233333 W 0.204444 0.266667
- [[119. 119.] [106. 106.]] 6.501704455367053
- array([[ 0.05, 1.37], [ 1.37, 186.56]])
- 0.4402088708468081

---

## 02-feature-engineering/wrapper-feature-selection

### Imports
- `import pandas as pd`
- `from sklearn.linear_model import LogisticRegression`
- `from mlxtend.feature_selection import SequentialFeatureSelector as SFS`
- `from mlxtend.plotting import plot_sequential_feature_selection as plot_sfs`
- `import matplotlib.pyplot as plt`
- `from sklearn.preprocessing import StandardScaler`
- `from sklearn.feature_selection import RFE`
- `from sklearn.model_selection import train_test_split`

### Headings
- ## Wrapper Methods: Feature Selection for Obesity Prediction
- ## Evaluating a Logistic Regression Model
- ### Split the data into `X` and `y`
- ### Logistic regression model
- ### Fit the model
- ### Model accuracy
- ## Sequential Forward Selection
- ### Inspect the results
- ### Visualize model accuracy
- ## Sequential Backward Selection
- ## Recursive Feature Elimination
- ### Standardize the data
- ### Recursive feature elimination model
- ### Inspect chosen features

### Result-oriented markdown
- ## Wrapper Methods: Feature Selection for Obesity Prediction In this project, you'll analyze data from a survey conducted by Fabio Mendoza Palechor and Alexis de la Hoz Manotas that asked people about their eating habits and weight. The data was obtained from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition+). Categorical variables were changed to numerical ones in order to facilitate analysis. First, you'll fit a logistic regression model to try to predict whether survey respondents are obese based on their answers to questions in the survey. After that, you'll use three different wrapper methods to choose a smaller feature subset. You'll use sequential forward selection, sequential backward floating selection, and recursive feature elimination. After implementing each wrapper method, you'll evaluate the model accuracy on the resulting smaller feature subsets and compare that with the model accuracy using all available features.
- ### Inspect the results Now that you've run the sequential forward selection algorithm on the logistic regression model with `X` and `y` you can see what features were chosen and check the model accuracy on the smaller feature set. Print `sfs.subsets_[9]` to inspect the results of sequential forward selection.
- ### Visualize model accuracy It can be helpful to visualize the results of sequential forward selection and see how accuracy is affected as each feature is added. Use the code `plot_sfs(sfs.get_metric_dict())` to plot the model accuracy as a function of the number of features used. Make sure to show your plot as well.
- ### Inspect the results Now that you've run the sequential backward selection algorithm on the logistic regression model with `X` and `y` you can see what features were chosen and check the model accuracy on the smaller feature set. Print `sbs.subsets_[7]` to inspect the results of sequential backward selection.
- ### Visualize model accuracy You can visualize the results of sequential backward floating selection just as you did with sequential forward selection. Use the code `plot_sfs(sbs.get_metric_dict())` to plot the model accuracy as a function of the number of features used.
- So far you've tried two different sequential feature selection methods. Let's try one more: recursive feature elimination. First you'll standardize the data, then you'll fit the RFE model and inspect the results. At a later step of this project, you'll need to be able to access feature names. Enter the code `features = X.columns` for use later.
- ### Inspect chosen features Now that you've fit the RFE model you can evaluate the results. Create a list of chosen feature names and call it `rfe_features`. You can use a list comprehension and filter the features in `zip(features, rfe.support_)` based on whether their support is `True` (meaning the model kept them) or `False` (meaning the model eliminated them).

### Metric/result code
- `accuracy = lr.score(X_test, y_test)`
- `scoring='accuracy',`
- `print('Best combination of SFS (ACC: %.3f): %s\n' % (sfs.subsets_[9]['avg_score'], sfs.subsets_[9]['feature_names']))`
- `print('Best combination of SBS (ACC: %.3f): %s\n' % (sbs.subsets_[7]['avg_score'], sbs.subsets_[7]['feature_names']))`
- `print(f"RFE with LR model Accuracy: {rfe.score(X_scaled, y)}")`

### Saved textual outputs
- Shape of X (predictor variables): (2111, 18) Shape of y (outcome variable): (2111,)
- LogisticRegression(max_iter=1000)
- SequentialFeatureSelector(cv=0, estimator=LogisticRegression(max_iter=1000), k_features=(9, 9), scoring='accuracy')
- Best combination of SFS (ACC: 0.783): ('Gender', 'Age', 'family_history_with_overweight', 'FAVC', 'CAEC', 'SMOKE', 'SCC', 'FAF', 'Motorbike')
- /Users/davidalmagro/Documents/projects/ml_env/lib/python3.12/site-packages/mlxtend/feature_selection/sequential_feature_selector.py:895: SmallSampleWarning: One or more sample arguments is too small; all returned values will be NaN. See documentation for sample size requirements. std_err = scipy.stats.sem(ary)
- (<Figure size 640x480 with 1 Axes>, <Axes: xlabel='Number of Features', ylabel='Performance'>)
- <Figure size 640x480 with 1 Axes>
- <Figure size 640x480 with 0 Axes>
- SequentialFeatureSelector(cv=0, estimator=LogisticRegression(max_iter=1000), forward=False, k_features=(7, 7), scoring='accuracy')
- Best combination of SBS (ACC: 0.764): ('Age', 'family_history_with_overweight', 'FAVC', 'FCVC', 'CAEC', 'CALC', 'Public_Transportation')
- RFE(estimator=LogisticRegression(max_iter=1000), n_features_to_select=7)
- Selected features by RFE: Index(['Age', 'family_history_with_overweight', 'FAVC', 'FCVC', 'CAEC', 'SCC', 'Automobile'], dtype='object')
- RFE with LR model Accuracy: 0.7626717195641876

---

## 03-supervised-learning/baseball-strike-zones-svm

### Imports
- `import pybaseball as pb`
- `import matplotlib.pyplot as plt`
- `import numpy as np`
- `from sklearn.svm import SVC`
- `from sklearn.model_selection import train_test_split`
- `from svm_visualization import draw_boundary`
- `from pybaseball import  playerid_lookup`
- `from pybaseball import  statcast_batter`

### Headings
- # Predicting and Visualizing Baseball Strike Zones With Machine Learning: Support Vector Machines
- ## Objective
- ## Tools and Techniques
- ## Insights

### Result-oriented markdown
- # Predicting and Visualizing Baseball Strike Zones With Machine Learning: Support Vector Machines In Major League Baseball (MLB), the **strike zone** is a critical component of the game. It determines whether a pitch is called a **strike** or a **ball**. While the strike zone has a strict rulebook definition, in practice, its boundaries can vary based on the **batter's height**, the **umpire's judgment**, and other contextual factors. In this project, we use **machine learning**—specifically **Support Vector Machines (SVMs)**—to analyze and visualize the "real strike zones" of three notable MLB players: 1. **Aaron Judge**: One of the tallest players in MLB history. 2. **Jose Altuve**: One of the shortest players in MLB history. 3. **David Ortiz**: A legendary power hitter with a unique approach to pitches. --- ## Objective The goal of this project is to: 1. Analyze pitch data for these players using **SVM classifiers** to identify decision boundaries that separate strikes and balls. 2. Visualize the **predicted strike zone** for each player based on pitch location (`plate_x` and `plate_z`). 3. Compare how the strike zones vary for players of different **physical builds**. --- ## To

### Metric/result code
- `accuracy = classifier.score(validation_features, validation_labels)`
- `print(f"Classifier accuracy on the validation set: {accuracy*100:.2f}%")`
- `best_accuracy = 0`
- `print(f"C: {C:.2f}, Gamma: {gamma:.2f}, Accuracy: {accuracy*100:.4f}%")`
- `if accuracy > best_accuracy:`
- `best_accuracy = accuracy`
- `print(f"Best configuration -> C: {best_C:.2f}, Gamma: {best_gamma:.2f}, Accuracy: {best_accuracy*100:.4f}%")`

### Saved textual outputs
- ['swinging_strike' 'hit_into_play' 'foul' 'ball' 'blocked_ball' 'called_strike' 'foul_tip' 'swinging_strike_blocked' 'hit_by_pitch'] ['S' 'X' 'B'] 0 S 1 S 2 S 3 X 4 X .. 3386 X 3387 S 3388 S 3389 X 3390 S Name: type, Length: 3391, dtype: object
- 0 NaN 1 1.0 2 0.0 3 0.0 4 0.0 ... 2649 NaN 2650 0.0 2651 0.0 2652 0.0 2653 NaN Name: type, Length: 2654, dtype: float64
- plate_x plate_z 0 0.38 0.78 1 0.46 1.11 2 0.63 0.80 3 0.26 1.82 4 0.34 2.37 plate_x plate_z 0 -0.71 2.81 1 -0.66 1.58 2 1.08 2.26 3 0.72 3.44 4 -1.04 3.36 Empty DataFrame Columns: [plate_x, plate_z] Index: []
- Aaron Judge NaN check: plate_x 0 plate_z 0 type 0 dtype: int64 Jose Altuve NaN check: plate_x 0 plate_z 0 type 0 dtype: int64 David Ortiz NaN check: plate_x 0 plate_z 0 type 0 dtype: int64
- <Figure size 640x480 with 1 Axes>
- <Figure size 640x480 with 0 Axes>
- Classifier has been trained.
- /Users/davidalmagro/Documents/projects/ml_env/lib/python3.12/site-packages/sklearn/base.py:493: UserWarning: X does not have valid feature names, but SVC was fitted with feature names warnings.warn(
- Classifier accuracy on the validation set: 82.82%
- C: 0.01, Gamma: 0.01, Accuracy: 50.6873% C: 0.01, Gamma: 0.10, Accuracy: 71.8213% C: 0.01, Gamma: 1.00, Accuracy: 82.6460% C: 0.01, Gamma: 10.00, Accuracy: 65.8076% C: 0.01, Gamma: 100.00, Accuracy: 50.6873% C: 0.10, Gamma: 0.01, Accuracy: 73.3677% C: 0.10, Gamma: 0.10, Accuracy: 81.6151% C: 0.10, Gamma: 1.00, Accuracy: 82.8179% C: 0.10, Gamma: 10.00, Accuracy: 83.1615% C: 0.10, Gamma: 100.00, Accuracy: 77.1478% C: 1.00, Gamma: 0.01, Accuracy: 73.5395% C: 1.00, Gamma: 0.10, Accuracy: 82.3024% C: 1.00, Gamma: 1.00, Accuracy: 83.1615% C: 1.00, Gamma: 10.00, Accuracy: 83.3333% C: 1.00, Gamma: 100.00, Accuracy: 82.6460% C: 10.00, Gamma: 0.01, Accuracy: 80.5842% C: 10.00, Gamma: 0.10, Accuracy: 82.9897% C: 10.00, Gamma: 1.00, Accuracy: 82.6460% C: 10.00, Gamma: 10.00, Accuracy: 82.8179% C: 10.00, Gamma: 100.00, Accuracy: 79.0378% C: 100.00, Gamma: 0.01, Accuracy: 81.4433% C: 100.00, Gamma: 0.10, Accuracy: 82.8179% C: 100.00, Gamma: 1.00, Accuracy: 82.9897% C: 100.00, Gamma: 10.00, Accuracy:

---

## 03-supervised-learning/book-recommender-svm

### Imports
- `import pandas as pd`
- `from surprise import Reader`
- `from surprise import Dataset`
- `from surprise.model_selection import train_test_split`
- `from surprise import KNNBasic`
- `from surprise import accuracy`

### Headings
- # Book Recommender Prototype
- ## Features
- ## Goal
- ## Libraries Import & dataset download
- ## Dataset Import
- # 1. Print Dataset Size and Examine Column Data Types
- # 2. Distribution of Ratings
- # 3. Filter Ratings That Are Out of Range
- # 4. Prepare Data for Surprise: Build a Surprise Reader Object
- # 5. Load `book_ratings` into a Surprise Dataset
- # 6. Create an 80:20 Train-Test Split and Set the Random State to 1
- # 7. Train a Collaborative Filter Using KNNBasic
- # 8. Evaluate the Recommender System
- # 9. Make a Prediction for a Specific User and Book

### Result-oriented markdown
- None found

### Metric/result code
- `from surprise import accuracy`
- `predictions = algo.test(testset)`
- `rmse = accuracy.rmse(predictions)`
- `print(f"RMSE: {rmse}")`
- `prediction = algo.predict(uid=user_id, iid=book_id)`
- `print(f"Predicted rating for user {user_id} and book {book_id}: {prediction.est:.2f}")`

### Saved textual outputs
- user_id book_id rating 0 d089c9b670c0b0b339353aebbace46a1 7686667 3 1 6dcb2c16e12a41ae0c6c38e9d46f3292 18073066 5 2 244e0ce681148a7586d7746676093ce9 13610986 5 3 73fcc25ff29f8b73b3a7578aec846394 27274343 1 4 f8880e158a163388a990b64fec7df300 11614718 4
- <class 'pandas.core.frame.DataFrame'> RangeIndex: 3500 entries, 0 to 3499 Data columns (total 3 columns): # Column Non-Null Count Dtype --- ------ -------------- ----- 0 user_id 3500 non-null object 1 book_id 3500 non-null int64 2 rating 3500 non-null int64 dtypes: int64(2), object(1) memory usage: 82.2+ KB None
- rating 0 120 1 125 2 269 3 707 4 1278 5 1001 Name: count, dtype: int64
- rating 1 125 2 269 3 707 4 1278 5 1001 Name: count, dtype: int64
- <surprise.reader.Reader object at 0x13d173aa0>
- Dataset loaded into Surprise format.
- Computing the msd similarity matrix... Done computing similarity matrix. Model trained successfully using KNNBasic.
- RMSE: 1.0427 RMSE: 1.0427242524656692
- Predicted rating for user 8842281e1d1347389f2ab93d60773d4d and book 18007564: 3.81

---

## 03-supervised-learning/car-acceptability-gradient-boosting

### Imports
- `import pandas as pd`
- `import numpy as np`
- `from sklearn.model_selection import train_test_split`
- `from sklearn.ensemble import GradientBoostingClassifier`
- `from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score, confusion_matrix`

### Headings
- # **Predicting Car Acceptability based on Price and Technical features: Gradient Boosting Classification**
- ## **Objective**
- ## **Dataset**
- ## **Implementation Steps**
- ### 1. **Model Creation**
- ### 2. **Model Training and Prediction**
- ### 3. **Model Evaluation**
- ### 4. **Confusion Matrix**
- ## **Outcome**
- ## **Key Highlights**

### Result-oriented markdown
- # **Predicting Car Acceptability based on Price and Technical features: Gradient Boosting Classification** ## **Objective** The project aims to implement a **Gradient Boosted Trees** classification model using `GradientBoostingClassifier` from the **scikit-learn** library to solve a classification problem. The goal is to evaluate the acceptability of a car based on its price and technical characteristics, utilizing a dataset sourced from **UCI’s Machine Learning Repository**. --- ## **Dataset** The dataset consists of labeled data for evaluating car acceptability, categorized based on various features including price and technical attributes. --- ## **Implementation Steps** ### 1. **Model Creation** - A `GradientBoostingClassifier` is instantiated with **15 estimators** (`n_estimators=15`) and all other parameters set to default. - The model parameters are printed using the `.get_params()` method to confirm the configuration. ### 2. **Model Training and Prediction** - The model is trained on the training dataset (`X_train` and `y_train`). - Predictions are made on the testing dataset (`X_test`), and the results are stored in a variable named `y_pred`. ### 3. **Model Evaluation** Th

### Metric/result code
- `from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score, confusion_matrix`
- `accuracy = accuracy_score(y_test, y_pred)`
- `precision = precision_score(y_test, y_pred)`
- `recall = recall_score(y_test, y_pred)`
- `f1 = f1_score(y_test, y_pred)`
- `print(f'Test set accuracy:\t{accuracy}')`
- `print(f'Test set precision:\t{precision}')`
- `print(f'Test set recall:\t{recall}')`
- `print(f'Test set f1-score:\t{f1}')`

### Saved textual outputs
- {'ccp_alpha': 0.0, 'criterion': 'friedman_mse', 'init': None, 'learning_rate': 0.1, 'loss': 'log_loss', 'max_depth': 3, 'max_features': None, 'max_leaf_nodes': None, 'min_impurity_decrease': 0.0, 'min_samples_leaf': 1, 'min_samples_split': 2, 'min_weight_fraction_leaf': 0.0, 'n_estimators': 15, 'n_iter_no_change': None, 'random_state': None, 'subsample': 1.0, 'tol': 0.0001, 'validation_fraction': 0.1, 'verbose': 0, 'warm_start': False} Test set accuracy: 0.8978805394990366 Test set precision: 0.7885714285714286 Test set recall: 0.8961038961038961 Test set f1-score: 0.8389057750759878 Confusion Matrix: predicted yes predicted no actual yes 138 16 actual no 37 328

---

## 03-supervised-learning/email-similarity-naive-bayes

### Imports
- `from sklearn.datasets import fetch_20newsgroups`
- `from sklearn.naive_bayes import MultinomialNB`
- `from sklearn.feature_extraction.text import CountVectorizer`
- `import random`

### Headings
- # Email Similarity Analysis using Naive Bayes Classification
- ## Introduction
- ### Objectives
- ### Key Questions
- ### Tools and Techniques
- ## First Steps
- ### Libraries and dataset import
- ## Train-Test split and data processing
- ## Training a Naive Bayes classification model
- ## Testing the model accuracy
- ## Testing different categories with a Function Abstraction

### Result-oriented markdown
- # Email Similarity Analysis using Naive Bayes Classification In this project, we aim to explore the similarities and distinctions between emails from different categories using **scikit-learn's Naive Bayes implementation**. By classifying emails into topics such as *hockey*, *soccer*, and *tech*, we will evaluate the ease or difficulty of distinguishing between these topics based on text content. ## Introduction ### Objectives - To classify emails into distinct categories using the Naive Bayes algorithm. - To measure the accuracy of the classifier for various datasets. - To determine which topics are more difficult to differentiate based on email content. ### Key Questions 1. How challenging is it to differentiate between emails about hockey and soccer? 2. How does the difficulty compare when distinguishing between hockey and tech-related emails? By analyzing the classifier's performance across multiple datasets, we will uncover insights into the inherent similarities between different topics and the limitations of text-based classification. ### Tools and Techniques - **Programming Language**: Python - **Libraries**: scikit-learn, pandas, numpy - **Methods**: Text preprocessing, TF

### Metric/result code
- `accuracy = classifier.score(test_counts, test_emails.target)`
- `print(f"Classifier Accuracy: {accuracy*100:.2f}%")`
- `float: Accuracy of the classifier on the test set.`
- `return accuracy`
- `accuracy = train_and_evaluate(categories)`
- `results.append((categories, accuracy))`
- `print(f"Categories: {categories}, Accuracy: {accuracy:.2f}")`

### Saved textual outputs
- MultinomialNB()
- Classifier Accuracy: 97.24%
- Categories: ['rec.sport.hockey', 'sci.space'], Accuracy: 0.99 Categories: ['alt.atheism', 'talk.politics.misc'], Accuracy: 0.96 Categories: ['comp.sys.mac.hardware', 'comp.windows.x'], Accuracy: 0.96 Categories: ['comp.windows.x', 'comp.graphics'], Accuracy: 0.86 Categories: ['alt.atheism', 'talk.politics.mideast'], Accuracy: 0.95

---

## 03-supervised-learning/income-prediction-random-forest

### Imports
- `import pandas as pd`
- `import numpy as np`
- `import matplotlib.pyplot as plt`
- `import seaborn as sns`
- `from sklearn.model_selection import train_test_split`
- `from sklearn.tree import DecisionTreeClassifier`
- `from sklearn.ensemble import RandomForestClassifier, BaggingClassifier, RandomForestRegressor`
- `from sklearn import tree`
- `from sklearn.linear_model import LogisticRegression`
- `from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score, roc_auc_score`

### Headings
- # Predicting Income based on Census Data: Random Forest Classifier
- ## Dataset Details
- ## Data investigation
- ### Libraries loading
- ### Data preview and analysis
- ## Train-Test split
- ## Random Forest Baseline
- ## Random Forest Hyperparameter Tunning
- ## Model refit with optimal hyperparameters (depth)
- ## Additional Features creation and model Re-Tuning
- ## Tune of Model with new features
- ### Visualisation of accuracy comparison: New Model vs Previous One:
- ### Final Note

### Result-oriented markdown
- ### Final Note This project could be extended by considering hyperparameter tuning based on a different evaluation metric. Since the target variable classes are fairly imbalanced, using metrics such as **AUC** or **F1 score** instead of accuracy may lead to different results. This approach could help optimize the model for better performance on imbalanced

### Metric/result code
- `from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score, roc_auc_score`
- `accuracy = rf_classifier.score(X_test, y_test)`
- `print(f"Baseline Accuracy of RandomForestClassifier: {accuracy:.2f}")`
- `accuracy_train = []`
- `accuracy_test = []`
- `train_accuracy = rf_classifier.score(X_train, y_train)`
- `accuracy_train.append(train_accuracy)`
- `test_accuracy = rf_classifier.score(X_test, y_test)`
- `accuracy_test.append(test_accuracy)`
- `print("Training Accuracy:", accuracy_train)`
- `print("Testing Accuracy:", accuracy_test)`
- `max_accuracy = max(accuracy_test)`
- `optimal_depth = accuracy_test.index(max_accuracy) + 1  # +1 since depth starts at 1`
- `print(f"The largest accuracy on the test data is {max_accuracy:.4f}, occurring at max_depth = {optimal_depth}.")`
- `plt.plot(depths, accuracy_train, label="Training Accuracy", marker='o')`
- `plt.plot(depths, accuracy_test, label="Test Accuracy", marker='o')`
- `plt.title("Model Accuracy vs. Max Depth", fontsize=14)`
- `plt.ylabel("Accuracy", fontsize=12)`
- `accuracy_train_new = []`
- `accuracy_test_new = []`
- `train_accuracy_new = rf_classifier_new.score(X_new_train, y_train)`
- `accuracy_train_new.append(train_accuracy_new)`
- `test_accuracy_new = rf_classifier_new.score(X_new_test, y_test)`
- `accuracy_test_new.append(test_accuracy_new)`
- `print("New Training Accuracy:", accuracy_train_new)`

### Saved textual outputs
- <Figure size 600x400 with 1 Axes>
- Output variable (y): 0 0 1 0 2 0 3 0 4 0 Name: income, dtype: int64 Percentage Distribution of y: 0 (<=50K): 75.92% 1 (>50K): 24.08%
- Baseline Accuracy of RandomForestClassifier: 0.82
- Training Accuracy: [0.7999846437346437, 0.800637285012285, 0.8100429975429976, 0.8175675675675675, 0.8180666461916462, 0.8200629606879607, 0.8205236486486487, 0.8226735257985258, 0.8244394963144963, 0.8261286855036855, 0.8324247542997543, 0.8366861179361179, 0.8392582923832924, 0.8420608108108109, 0.84432585995086, 0.8455927518427518, 0.8498541154791155, 0.8533476658476659, 0.8548065110565111, 0.8568412162162162, 0.8579929361179361, 0.858914312039312, 0.8597972972972973, 0.8603731572481572, 0.8606035012285013] Testing Accuracy: [0.8105327805926609, 0.8109933978197451, 0.820205742361431, 0.8292645478274221, 0.8297251650545063, 0.8303393213572854, 0.8303393213572854, 0.8304928604329802, 0.831260555811454, 0.8301857822815907, 0.8323353293413174, 0.8346384154767388, 0.8340242591739597, 0.8320282511899278, 0.8324888684170121, 0.8335636419468755, 0.8306463995086749, 0.8265008444649163, 0.8255796100107478, 0.8255796100107478, 0.822201750345463, 0.8229694457239367, 0.822815906648242, 0.8206663
- The largest accuracy on the test data is 0.8346, occurring at max_depth = 12.
- <Figure size 1000x600 with 1 Axes>
- <Figure size 640x480 with 0 Axes>
- Top 5 Features: Feature Importance 1 capital-gain 0.370119 0 age 0.248969 3 hours-per-week 0.140480 2 capital-loss 0.140439 4 sex_Male 0.078258
- New Training Accuracy: [0.7640509828009828, 0.8027103808353808, 0.8154944717444718, 0.8205620393120393, 0.8305820024570024, 0.8339603808353808, 0.8352656633906634, 0.8366477272727273, 0.8382217444717445, 0.8453624078624079, 0.8485488329238329, 0.851159398034398, 0.8556511056511057, 0.8591062653562653, 0.8625614250614251, 0.8660549754299754, 0.8697404791154791, 0.8726965601965602, 0.8755374692874693, 0.878762285012285, 0.8807202088452089, 0.8830620393120393, 0.8840218058968059, 0.8855190417690417, 0.8862484643734644] New Testing Accuracy: [0.7782895746967603, 0.8136035621065562, 0.8246583755565792, 0.8298787041302012, 0.8386304314448026, 0.8426224474128666, 0.8430830646399509, 0.8438507600184247, 0.844311377245509, 0.8479963150621833, 0.8476892369107938, 0.8493781667434362, 0.8486104713649624, 0.8498387839705205, 0.8498387839705205, 0.8487640104406572, 0.8486104713649624, 0.8473821587594043, 0.8475356978350991, 0.8444649163212038, 0.8432366037156457, 0.8415476738830032, 0.84001228312605
- New Model: Largest accuracy on test data is 0.8498 at max_depth = 14. Previous Model: Largest accuracy on test data is 0.8346 at max_depth = 12. The new model with 'education_bin' outperforms the previous model.
- <Figure size 1200x600 with 1 Axes>

---

## 03-supervised-learning/raisin-classification

### Imports
- `import pandas as pd`
- `from sklearn.model_selection import train_test_split`
- `from sklearn.tree import DecisionTreeClassifier`
- `from sklearn.linear_model import LogisticRegression`
- `from sklearn.model_selection import GridSearchCV`
- `from sklearn.model_selection import RandomizedSearchCV`
- `from scipy.stats import uniform`

### Headings
- # Feature Engineering - Regularisation: Classifying Raisins with Hyperparameter Tuning
- ## Project Goals
- ## Dataset Overview
- ### Dataset Information
- ### 1. Explore the Dataset
- ### 2. Grid Search with Decision Tree Classifier
- ### 2. Random Search with Logistic Regression

### Result-oriented markdown
- None found

### Metric/result code
- `print(f"Best Cross-Validation Accuracy:{gscv.best_score_}")`
- `test_score = best_gscv_tree.score(X_test, y_test)`
- `print(f"Test Data Accuracy:{test_score}")`
- `mean_test_scores = gscv.cv_results_['mean_test_score']`
- `scores_df = pd.DataFrame(mean_test_scores, columns=['Mean Test Score'])`
- `results_df = pd.concat([params_df, scores_df], axis=1)`
- `print("Best Cross-Validation Accuracy:", clf.best_score_)`
- `mean_test_scores = clf.cv_results_['mean_test_score']`

### Saved textual outputs
- Number of unique classes: 2
- Total number of features: 7 Total number of samples: 900 Samples belonging to class '1': 450
- GridSearchCV(estimator=DecisionTreeClassifier(random_state=19), param_grid={'max_depth': [3, 5, 7], 'min_samples_split': [2, 3, 4]})
- Best Estimator Hyperparameters:DecisionTreeClassifier(max_depth=3, random_state=19) Best Cross-Validation Accuracy:0.8541666666666667 Test Data Accuracy:0.8555555555555555
- max_depth min_samples_split Mean Test Score 0 3 2 0.854167 1 3 3 0.854167 2 3 4 0.854167 3 5 2 0.851389 4 5 3 0.851389 5 5 4 0.851389 6 7 2 0.819444 7 7 3 0.820833 8 7 4 0.820833
- RandomizedSearchCV(estimator=LogisticRegression(max_iter=1000, random_state=19, solver='liblinear'), n_iter=8, param_distributions={'C': <scipy.stats._distn_infrastructure.rv_continuous_frozen object at 0x14f9c8470>, 'penalty': ['l1', 'l2']}, random_state=19)
- Best Estimator from Random Search: LogisticRegression(C=67.19770812804666, max_iter=1000, random_state=19, solver='liblinear'), Penalty: l2 Best Cross-Validation Accuracy: 0.8708333333333333 Summary of Random Search Results: C penalty Mean Test Score 0 9.753360 l2 0.869444 1 41.274294 l2 0.869444 2 13.813169 l2 0.869444 3 67.563267 l1 0.868056 4 67.197708 l2 0.870833 5 0.814826 l1 0.868056 6 63.566073 l2 0.869444 7 84.901482 l2 0.869444

---

## 03-supervised-learning/wine-quality-regularization

### Imports
- `import numpy as np`
- `import pandas as pd`
- `import matplotlib.pyplot as plt`
- `import seaborn as sns`
- `from sklearn.preprocessing import StandardScaler`
- `from sklearn.model_selection import train_test_split`
- `from sklearn.linear_model import LogisticRegression`
- `from sklearn.metrics import f1_score`
- `from sklearn.model_selection import GridSearchCV`
- `from sklearn.linear_model import LogisticRegressionCV`

### Headings
- # Predict Wine Quality with Regularization
- ## Introduction
- ## Goals
- ## Dataset Overview
- ## Source and Citation

### Result-oriented markdown
- # Predict Wine Quality with Regularization ## Introduction In this project, we will be working with data from the **Wine Quality Dataset** hosted on the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/186/wine+quality). Specifically, we’ll focus on the red wine data. While the original dataset assigns a quality rating from 1 to 10 for each wine, we have reframed the problem as a binary classification task: - **Good wine**: Quality rating > 5 (labeled as `1`) - **Bad wine**: Quality rating ≤ 5 (labeled as `0`) ## Goals The goals of this project are to: 1. Implement and evaluate different logistic regression classifiers. 2. Identify the best ridge-regularized classifier through hyperparameter tuning. 3. Develop a lasso-regularized feature selection approach to identify the most important input variables. ## Dataset Overview The dataset includes **11 input variables** derived from physicochemical tests: - `fixed acidity` - `volatile acidity` - `citric acid` - `residual sugar` - `chlorides` - `free sulfur dioxide` - `total sulfur dioxide` - `density` - `pH` - `sulphates` - `alcohol` The **output variable** is `quality`, represented as a binary classification (`0` 

### Metric/result code
- `coefficients = clf_no_reg.coef_.ravel()`
- `coef = pd.Series(coefficients,predictors).sort_values()`
- `coef.plot(kind='bar', title = 'Coefficients (no regularization)')`
- `from sklearn.metrics import f1_score`
- `print('Training Score', f1_score(y_train, y_pred_train))`
- `print('Testing Score', f1_score(y_test, y_pred_test))`
- `print('Training Score for L2-reg (default)', f1_score(y_train, y_pred_train_def))`
- `print('Testing Score for L2-reg (default)', f1_score(y_test, y_pred_test_def))`
- `test_array.append(f1_score(y_test, y_pred_test_def_c))`
- `training_array.append(f1_score(y_train, y_pred_train_def_c))`
- `plt.plot(C_array,training_array, label='Training F1 Score')`
- `plt.plot(C_array,test_array, label='Test F1 Score')`
- `plt.ylabel('f1 score')`
- `scoring = 'f1',`
- `print(f"The best f1 score comes from C={grid_search.best_params_['C']:.6f} and is f1={grid_search.best_score_:.4f}")`
- `test_f1_score_gs = f1_score(y_test, y_pred_gs)`
- `print(f"Executing the logreg with the same C (C = {grid_search.best_params_['C']:.6f}) for the test dataset, now f1 is: {test_f1_score_gs:.4f}")`
- `scoring='f1',       # F1 score as the metric`
- `print(f"Mean cross-validated F1 score for best C-value: {clf_l1.scores_[1].mean(axis=0).max():.4f}")`
- `coefficients = clf_l1.coef_.ravel()`
- `coef.plot(kind='bar', title = 'Coefficients for tuned L1')`

### Saved textual outputs
- Index(['fixed acidity', 'volatile acidity', 'citric acid', 'residual sugar', 'chlorides', 'free sulfur dioxide', 'total sulfur dioxide', 'density', 'pH', 'sulphates', 'alcohol', 'quality'], dtype='object')
- <Figure size 640x480 with 1 Axes>
- <Figure size 640x480 with 0 Axes>
- Training Score 0.7727598566308244 Testing Score 0.7266666666666667
- Training Score for L2-reg (default) 0.7727598566308244 Testing Score for L2-reg (default) 0.7266666666666667
- GridSearchCV(cv=5, estimator=LogisticRegression(solver='liblinear'), param_grid={'C': array([0.0001 , 0.00010476, 0.00010975, 0.00011498, 0.00012045, 0.00012619, 0.00013219, 0.00013849, 0.00014508, 0.00015199, 0.00015923, 0.00016681, 0.00017475, 0.00018307, 0.00019179, 0.00020092, 0.00021049, 0.00022051, 0.00023101, 0.00024201, 0.00025354, 0.00026561, 0.00027826, 0.00029151,... 0.00205651, 0.00215443, 0.00225702, 0.00236449, 0.00247708, 0.00259502, 0.00271859, 0.00284804, 0.00298365, 0.00312572, 0.00327455, 0.00343047, 0.00359381, 0.00376494, 0.00394421, 0.00413201, 0.00432876, 0.00453488, 0.00475081, 0.00497702, 0.00521401, 0.00546228, 0.00572237, 0.00599484, 0.00628029, 0.00657933, 0.00689261, 0.00722081, 0.00756463, 0.00792483, 0.00830218, 0.00869749, 0.00911163, 0.00954548, 0.01 ])}, scoring='f1')
- The best f1 score comes from C=0.006893 and is f1=0.7551
- Executing the logreg with the same C (C = 0.006893) for the test dataset, now f1 is: 0.6831
- LogisticRegressionCV(Cs=array([1.00000000e-02, 1.09749877e-02, 1.20450354e-02, 1.32194115e-02, 1.45082878e-02, 1.59228279e-02, 1.74752840e-02, 1.91791026e-02, 2.10490414e-02, 2.31012970e-02, 2.53536449e-02, 2.78255940e-02, 3.05385551e-02, 3.35160265e-02, 3.67837977e-02, 4.03701726e-02, 4.43062146e-02, 4.86260158e-02, 5.33669923e-02, 5.85702082e-02, 6.42807312e-02, 7.05... 1.70735265e+01, 1.87381742e+01, 2.05651231e+01, 2.25701972e+01, 2.47707636e+01, 2.71858824e+01, 2.98364724e+01, 3.27454916e+01, 3.59381366e+01, 3.94420606e+01, 4.32876128e+01, 4.75081016e+01, 5.21400829e+01, 5.72236766e+01, 6.28029144e+01, 6.89261210e+01, 7.56463328e+01, 8.30217568e+01, 9.11162756e+01, 1.00000000e+02]), cv=5, max_iter=1000, penalty='l1', scoring='f1', solver='liblinear')
- Best C value for LogRegCV: 0.25950242113997374 Mean cross-validated F1 score for best C-value: 0.7485
- <Figure size 1200x800 with 1 Axes>

---

## 04-unsupervised-learning/handwriting-recognition-kmeans

### Imports
- `import numpy as np`
- `from matplotlib import pyplot as plt`
- `from sklearn import datasets`
- `from sklearn.cluster import KMeans`

### Headings
- # Exploring K-Means Clustering for Handwriting Recognition
- ## Importing the Digits Dataset from Scikit Learn
- ## Image Visualisation
- ## K-Means Clustering
- ## K-Means visualisation
- ## Testing the model

### Result-oriented markdown
- None found

### Metric/result code
- `from sklearn.cluster import KMeans`
- `model = KMeans(n_clusters=10, random_state=seed)`
- `fig.suptitle("K-Means Visualisation")`
- `ax.imshow(model.cluster_centers_[i].reshape((8, 8)), cmap=plt.cm.binary)`

### Saved textual outputs
- (1797, 64) {'data': array([[ 0., 0., 5., ..., 0., 0., 0.], [ 0., 0., 0., ..., 10., 0., 0.], [ 0., 0., 0., ..., 16., 9., 0.], ..., [ 0., 0., 1., ..., 6., 0., 0.], [ 0., 0., 2., ..., 12., 0., 0.], [ 0., 0., 10., ..., 12., 1., 0.]]), 'target': array([0, 1, 2, ..., 8, 9, 8]), 'frame': None, 'feature_names': ['pixel_0_0', 'pixel_0_1', 'pixel_0_2', 'pixel_0_3', 'pixel_0_4', 'pixel_0_5', 'pixel_0_6', 'pixel_0_7', 'pixel_1_0', 'pixel_1_1', 'pixel_1_2', 'pixel_1_3', 'pixel_1_4', 'pixel_1_5', 'pixel_1_6', 'pixel_1_7', 'pixel_2_0', 'pixel_2_1', 'pixel_2_2', 'pixel_2_3', 'pixel_2_4', 'pixel_2_5', 'pixel_2_6', 'pixel_2_7', 'pixel_3_0', 'pixel_3_1', 'pixel_3_2', 'pixel_3_3', 'pixel_3_4', 'pixel_3_5', 'pixel_3_6', 'pixel_3_7', 'pixel_4_0', 'pixel_4_1', 'pixel_4_2', 'pixel_4_3', 'pixel_4_4', 'pixel_4_5', 'pixel_4_6', 'pixel_4_7', 'pixel_5_0', 'pixel_5_1', 'pixel_5_2', 'pixel_5_3', 'pixel_5_4', 'pixel_5_5', 'pixel_5_6', 'pixel_5_7', 'pi
- .. _digits_dataset: Optical recognition of handwritten digits dataset -------------------------------------------------- **Data Set Characteristics:** :Number of Instances: 1797 :Number of Attributes: 64 :Attribute Information: 8x8 image of integer pixels in the range 0..16. :Missing Attribute Values: None :Creator: E. Alpaydin (alpaydin '@' boun.edu.tr) :Date: July; 1998 This is a copy of the test set of the UCI ML hand-written digits datasets https://archive.ics.uci.edu/ml/datasets/Optical+Recognition+of+Handwritten+Digits The data set contains images of hand-written digits: 10 classes where each class refers to a digit. Preprocessing programs made available by NIST were used to extract normalized bitmaps of handwritten digits from a preprinted form. From a total of 43 people, 30 contributed to the training set and different 13 to the test set. 32x32 bitmaps are divided into nonoverlapping blocks of 4x4 and the number of on pixels are counted in each block. This generates an in
- [[ 0. 0. 5. ... 0. 0. 0.] [ 0. 0. 0. ... 10. 0. 0.] [ 0. 0. 0. ... 16. 9. 0.] ... [ 0. 0. 1. ... 6. 0. 0.] [ 0. 0. 2. ... 12. 0. 0.] [ 0. 0. 10. ... 12. 1. 0.]]
- [0 1 2 ... 8 9 8]
- <Figure size 640x480 with 0 Axes>
- <Figure size 480x480 with 1 Axes>
- 4
- KMeans(n_clusters=10, random_state=42)
- <Figure size 800x300 with 10 Axes>
- 0383

---

## 04-unsupervised-learning/olivetti-faces-pca

### Imports
- `import numpy as np`
- `from sklearn import datasets`
- `import matplotlib.pyplot as plt`
- `import pandas as pd`
- `from sklearn.decomposition import PCA`

### Headings
- # Olivetti Faces: Principal Component Analysis (PCA) for Image Data
- ## Motivation
- ## Objectives
- ## Significance
- ## Tools & Libraries
- ## Outcomes
- ## PART I - Data Standarization
- ## Part II - Dimensionality Reduction with PCA

### Result-oriented markdown
- # Olivetti Faces: Principal Component Analysis (PCA) for Image Data In this project, we explore the powerful dimensionality reduction technique **Principal Component Analysis (PCA)** using the **Olivetti Faces Dataset**, a collection of grayscale face images. PCA is a statistical method that transforms high-dimensional data into a smaller set of principal components while retaining as much variance (information) as possible. This project demonstrates the ability of PCA to compress and reconstruct image data, offering insights into its mechanisms and practical applications. --- ## Motivation High-dimensional datasets, such as images, are computationally expensive to process and analyze. Each image in the dataset can be represented as a vector of pixel intensities, resulting in thousands of features per image. This dimensionality makes tasks like visualization, analysis, and storage challenging. **Principal Component Analysis (PCA)** addresses this challenge by reducing the dimensionality of the data while preserving its essential features. By transforming images into a smaller number of principal components, PCA simplifies the dataset without significant loss of information. --- ## 

### Metric/result code
- `faces_mean = faces.mean(axis=0)`
- `faces_standardized = (faces - faces_mean) / faces_std`
- `pca = PCA(n_components=400)`
- `eigenfaces = pca.components_`
- `principal_components = pca.transform(faces_standardized)`
- `faces_reconstructed = pca.inverse_transform(principal_components)`
- `fig.suptitle('Reconstructed Images from Principal Components')`

### Saved textual outputs
- Number of features(pixels) per image: 4096 Square image side length: 64
- <Figure size 1000x800 with 15 Axes>
- PCA(n_components=400)

---

## 04-unsupervised-learning/particle-classification-pca

### Imports
- `import numpy as np`
- `import pandas as pd`
- `import matplotlib.pyplot as plt`
- `import seaborn as sns`
- `from sklearn.decomposition import PCA`
- `from sklearn.svm import SVC`
- `from sklearn.model_selection import train_test_split`
- `from sklearn.metrics import accuracy_score`

### Headings
- # Particle Classification with PCA: Gamma vs. Hadrons
- ## Introduction
- ## PART I: Variance Explained and Dimensionality Reduction for Telescope Particle Classification
- ### Dataset Observation
- ### Understanding influence of features by their variance: Eigen Values and vectors
- ## PART II: Principal Component Analysis
- ### Matrix standarization
- ### PCA execution
- ### Projection of our dataset onto the 2 principal axes
- ### Projection visualization
- ### Training a Support Vector Classifier with the 2 main components
- ### Training a Support Vector Classifier with the first 2 features of the standarised matrix

### Result-oriented markdown
- ## PART I: Variance Explained and Dimensionality Reduction for Telescope Particle Classification ### Dataset Observation

### Metric/result code
- `print("Cumulative percentages of variance explained:")`
- `mean = np.mean(data_matrix, axis=0)`
- `data_matrix_standardized = (data_matrix - mean) / std`
- `eigenvalues = pca.explained_variance_`
- `eigenvectors = pca.components_`
- `variance_ratios = pca.explained_variance_ratio_`
- `print("Variance Ratios (Proportion of Variance Explained):")`
- `print(variance_ratios)`
- `pca_2 = PCA(n_components=2)`
- `plt.title("Projection of Dataset onto First 2 Principal Components", fontsize=16)`
- `plt.xlabel("Principal Component 1 (PC1)", fontsize=12)`
- `plt.ylabel("Principal Component 2 (PC2)", fontsize=12)`
- `from sklearn.metrics import accuracy_score`
- `score = accuracy_score(y_test, y_pred)`
- `print("Accuracy of the SVC on PCA-transformed data (2 components):", score)`
- `score_original_features = accuracy_score(y_test_original, y_pred_original)`
- `print("Accuracy of the SVC using the first two features of the original standardized data matrix:")`
- `print(score_original_features)`

### Saved textual outputs
- fLength 0 fWidth 0 fSize 0 fConc 0 fConc1 0 fAsym 0 fM3Long 0 fM3Trans 0 fAlpha 0 fDist 0 class 0 dtype: int64
- <Axes: >
- <Figure size 1000x1000 with 2 Axes>
- Cumulative percentages of variance explained: [0.28849923 0.30931684 0.33476719 0.39989289 0.52372205 0.60311632 0.70424496 0.80183022 0.9014497 1. ]
- Variance Ratios (Proportion of Variance Explained): [0.28849923 0.12382916 0.10112864 0.09961948 0.0985503 0.09758527 0.07939426 0.0651257 0.02545035 0.02081761]
- PCA Transformed Data (2 Principal Axes): [[-1.30626818 0.17105677] [-0.94994367 0.45754399] [ 5.84120467 0.5834159 ] ... [ 1.94387036 0.95394554] [ 4.76409928 -0.27479141] [ 4.28118695 -3.65026249]]
- <Figure size 1108.88x700 with 1 Axes>
- Accuracy of the SVC on PCA-transformed data (2 components): 0.7105678233438486
- Accuracy of the SVC using the first two features of the original standardized data matrix: 0.7200315457413249

---

## 05-neural-networks/heart-failure-deep-learning

### Imports
- `import pandas as pd`
- `from sklearn.preprocessing import StandardScaler, LabelEncoder`
- `from sklearn.model_selection import train_test_split`
- `from collections import Counter`
- `from sklearn.compose import ColumnTransformer`
- `from tensorflow.keras.models import Sequential`
- `from tensorflow.keras.layers import Dense, InputLayer`
- `from sklearn.metrics import classification_report`
- `from tensorflow.keras.utils import to_categorical`
- `import numpy as np`

### Headings
- # Cardiovascular Diseases (CDVs) Detection with Deep Learning
- ## Introduction
- ## Dataset Overview
- ### Acknowledgments
- ## Objective
- ## Why This Matters
- ### Data Loading and analysis
- ### Data Prepraration before applying models
- ### Model Set-up
- ### Model Fit and Performance Analysis
- ### Updated Summary of the Classification Report
- ### Key Observations:
- ### Recommendations:

### Result-oriented markdown
- # Cardiovascular Diseases (CDVs) Detection with Deep Learning ## Introduction Cardiovascular diseases (CVDs) are the leading cause of death globally, accounting for approximately 31% of all deaths worldwide. Among the many manifestations of CVDs, heart failure is a significant contributor, causing widespread mortality and reduced quality of life. This project leverages a clinical dataset from Kaggle to develop a machine learning model that predicts patient survival after heart failure. By analyzing features such as age, serum creatinine, ejection fraction, and comorbidities (e.g., anemia, diabetes), this model aims to assist healthcare professionals in identifying high-risk patients and improving treatment strategies. ## Dataset Overview The dataset used in this project is publicly available on Kaggle: [Heart Failure Clinical Records Dataset](https://www.kaggle.com/datasets/andrewmvd/heart-failure-clinical-data). It contains information on 299 patients with 12 clinical features, including: - Demographics (e.g., age, sex) - Laboratory findings (e.g., serum creatinine, serum sodium) - Clinical history (e.g., presence of diabetes, high blood pressure) - Outcome (survival status) ### A
- ### Updated Summary of the Classification Report 1. **Overall Accuracy**: - The model achieved an overall accuracy of **78%** on the test data, meaning that 78% of the predictions correctly classified whether or not there was a death event. 2. **Performance for Patients Without a Death Event (Class 0)**: - **Precision**: 0.74 – Of all predictions made for "no death event," 74% were correct. - **Recall**: 0.97 – The model successfully identified 97% of patients who truly did not experience a death event. - **F1-score**: 0.84 – A strong balance between precision and recall for predicting no death event. - **Support**: 35 patients in the test set did not experience a death event. 3. **Performance for Patients With a Death Event (Class 1)**: - **Precision**: 0.93 – Of all predictions made for "death event," 93% were correct. - **Recall**: 0.52 – The model correctly identified only 52% of patients who truly experienced a death event. - **F1-score**: 0.67 – Indicates moderate performance in predicting death events due to the lower recall. - **Support**: 25 patients in the test set experienced a death event. 4. **Macro Average**: - **Precision**: 0.83 – Average precision across both class

### Metric/result code
- `metrics=['accuracy']`
- `print(f"Test Accuracy: {acc}")`
- `print(y_estimate[:5]) # The output is a probability distribution for each class, e.g., [0.1, 0.9] means 10% for class 0 and 90% for class 1`

### Saved textual outputs
- Counter({0: 203, 1: 96})
- X_train shape: (239, 12) X_test shape: (60, 12) Y_train shape: (239,) Y_test shape: (60,)
- Column order after transformation: ['age', 'creatinine_phosphokinase', 'ejection_fraction', 'platelets', 'serum_creatinine', 'serum_sodium', 'time', 'anaemia', 'diabetes', 'high_blood_pressure', 'sex', 'smoking']
- <Sequential name=sequential_3, built=False>
- [1mModel: "sequential_3"[0m
- ┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━┓ ┃[1m [0m[1mLayer (type) [0m[1m [0m┃[1m [0m[1mOutput Shape [0m[1m [0m┃[1m [0m[1m Param #[0m[1m [0m┃ ┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━┩ └─────────────────────────────────┴────────────────────────┴───────────────┘
- [1m Total params: [0m[38;5;34m0[0m (0.00 B)
- [1m Trainable params: [0m[38;5;34m0[0m (0.00 B)
- [1m Non-trainable params: [0m[38;5;34m0[0m (0.00 B)
- [1m Total params: [0m[38;5;34m156[0m (624.00 B)
- [1m Trainable params: [0m[38;5;34m156[0m (624.00 B)
- [1m Total params: [0m[38;5;34m182[0m (728.00 B)
- [1m Trainable params: [0m[38;5;34m182[0m (728.00 B)
- Epoch 1/100 [1m15/15[0m [32m━━━━━━━━━━━━━━━━━━━━[0m[37m[0m [1m1s[0m 11ms/step - accuracy: 0.5988 - loss: 0.7582 Epoch 2/100 [1m15/15[0m [32m━━━━━━━━━━━━━━━━━━━━[0m[37m[0m [1m0s[0m 9ms/step - accuracy: 0.6888 - loss: 0.5982 Epoch 3/100 [1m15/15[0m [32m━━━━━━━━━━━━━━━━━━━━[0m[37m[0m [1m0s[0m 9ms/step - accuracy: 0.6971 - loss: 0.5616 Epoch 4/100 [1m15/15[0m [32m━━━━━━━━━━━━━━━━━━━━[0m[37m[0m [1m0s[0m 9ms/step - accuracy: 0.7108 - loss: 0.5296 Epoch 5/100 [1m15/15[0m [32m━━━━━━━━━━━━━━━━━━━━[0m[37m[0m [1m0s[0m 9ms/step - accuracy: 0.7855 - loss: 0.4997 Epoch 6/100 [1m15/15[0m [32m━━━━━━━━━━━━━━━━━━━━[0m[37m[0m [1m0s[0m 10ms/step - accuracy: 0.7566 - loss: 0.4950 Epoch 7/100 [1m15/15[0m [32m━━━━━━━━━━━━━━━━━━━━[0m[37m[0m [1m0s[0m 9ms/step - accuracy: 0.8038 - loss: 0.4444 Epoch 8/100 [1m15/15[0m [32m━━━━━━━━━━━━━━━━━━━━[0m[37m[0m [1m0s[0m 9ms/step - accuracy: 0.7864 - loss: 0.4704 Epoch 9/100 [1m15/15[0m [32m━━━━━━━━━━━━━━━
- [1m2/2[0m [32m━━━━━━━━━━━━━━━━━━━━[0m[37m[0m [1m0s[0m 31ms/step - accuracy: 0.7826 - loss: 0.5710 Test Loss: 0.5693067908287048 Test Accuracy: 0.7833333611488342
- [1m2/2[0m [32m━━━━━━━━━━━━━━━━━━━━[0m[37m[0m [1m0s[0m 19ms/step [[9.4264507e-01 5.7354953e-02] [9.9702042e-01 2.9795209e-03] [9.1280198e-01 8.7198094e-02] [2.0149213e-04 9.9979848e-01] [8.9440191e-01 1.0559808e-01]]
- [0 0 0 1 0]
- [0 0 1 1 0]
- Classification Report: precision recall f1-score support 0 0.74 0.97 0.84 35 1 0.93 0.52 0.67 25 accuracy 0.78 60 macro avg 0.83 0.75 0.75 60 weighted avg 0.82 0.78 0.77 60

---

## 05-neural-networks/logic-gates-perceptron

### Imports
- `from sklearn.linear_model import Perceptron`
- `import matplotlib.pyplot as plt`
- `import numpy as np`
- `from itertools import product`

### Headings
- # Modeling Logic Gates Using Perceptrons
- ## Introduction
- ## Logic Gate Tables
- ### AND Gate
- ### XOR Gate
- ## Training Perceptrons for Logic Gates
- ### Training the Perceptron
- ### Visualizing the Decision Boundary
- ### Experimenting with OR and XOR Gates
- ## Conclusion on Independent Separability
- ### Linearly Separable Data (AND and OR Gates)
- ### Non-Linearly Separable Data (XOR Gate)
- ### Key Insights
- ### Implications

### Result-oriented markdown
- ### Experimenting with OR and XOR Gates Change the labels to represent OR and XOR gates. Observe how the decision boundary changes and why the perceptron fails for XOR.
- ## Conclusion on Independent Separability In this project, we explored the concept of linear separability using perceptrons to model basic logic gates such as AND, OR, and XOR. Through our experiments, we observed the following: ### Linearly Separable Data (AND and OR Gates) - AND and OR gates are examples of linearly separable problems. A straight line (decision boundary) can successfully separate the data points into distinct classes. - The perceptron, being a linear model, was able to learn these gates effectively, achieving perfect accuracy. ### Non-Linearly Separable Data (XOR Gate) - XOR gate data is **not linearly separable**, meaning no straight line can divide the input space into the required classes. - The perceptron failed to learn the XOR gate because it can only find linear decision boundaries. This limitation highlights the fundamental restriction of single-layer perceptrons when dealing with non-linearly separable problems. ### Key Insights - The concept of linear separability is crucial for understanding the strengths and weaknesses of perceptrons. - While simple problems can be solved by single-layer perceptrons, more complex, non-linear problems (like XOR) requir

### Metric/result code
- `accuracy = classifier.score(data, labels)`
- `print(f"Accuracy of the perceptron on the {title}: {accuracy:.2f}")`
- `print(f"Testing {title} predictions:")`

### Saved textual outputs
- Accuracy of the perceptron on the AND Gate: 1.00 Testing AND Gate predictions: Input: [0 0], Predicted Output: 0 Input: [0 1], Predicted Output: 0 Input: [1 0], Predicted Output: 0 Input: [1 1], Predicted Output: 1
- <Figure size 800x600 with 2 Axes>
- Accuracy of the perceptron on the OR Gate: 1.00 Testing OR Gate predictions: Input: [0 0], Predicted Output: 0 Input: [0 1], Predicted Output: 1 Input: [1 0], Predicted Output: 1 Input: [1 1], Predicted Output: 1
- Accuracy of the perceptron on the XOR Gate: 0.50 Testing XOR Gate predictions: Input: [0 0], Predicted Output: 0 Input: [0 1], Predicted Output: 0 Input: [1 0], Predicted Output: 0 Input: [1 1], Predicted Output: 0

---

## 05-neural-networks/perceptron-from-scratch

### Imports
- None found

### Headings
- # Neural Networks: Simulating a perceptron class
- ## Project Overview
- ### 1. Perceptron Class
- ### 2. Training Data
- ## Perceptron Class Definition
- ## Creating and training a Perceptron instance

### Result-oriented markdown
- None found

### Metric/result code
- `prediction = self.activation(self.weighted_sum(inputs))`
- `error = actual - prediction`

### Saved textual outputs
- [-10, 10]

---
