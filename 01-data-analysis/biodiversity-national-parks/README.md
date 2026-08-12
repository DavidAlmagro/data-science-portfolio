# Biodiversity in U.S. National Parks

An exploratory analysis of species observations and conservation status across Bryce Canyon, Great Smoky Mountains, Yellowstone, and Yosemite National Parks.

**Originally developed (first GitHub commit): October 28, 2024 · [View original repository](https://github.com/DavidAlmagro/BiodiversityInNationalParks_USA)**

## 1. Technologies & Concepts

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- Data cleaning and exploratory data analysis
- Grouped aggregation and categorical analysis
- Biodiversity and conservation-status analysis
- Comparative data visualization

## 2. Key Findings

- The observations dataset contains 23,296 records covering 5,541 unique scientific names across four parks.
- Yellowstone has the largest total number of recorded observations in the dataset (1,443,562), followed by Yosemite (863,332), Bryce (576,025), and Great Smoky Mountains (431,820).
- The species-information dataset contains 5,824 records across seven biological categories and five conservation-status levels.
- Vascular plants dominate the catalog with 4,262 species records, substantially more than any other category; birds are the next largest category with 488.
- The analysis combines observation abundance with conservation information to compare biodiversity patterns and identify species requiring greater conservation attention.

## 3. How to Run

From this project directory:

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter pandas numpy matplotlib seaborn
jupyter notebook analysis.ipynb
```

The required datasets are included in `data/` and the notebook uses relative paths from this directory.
