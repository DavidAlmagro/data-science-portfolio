# Email Similarity with Naive Bayes

A text-classification exercise that uses newsgroup messages to study how easily different topics can be separated from their vocabulary.

## 1. Technologies & Concepts

- Python
- scikit-learn `MultinomialNB`
- `CountVectorizer`
- Bag-of-words text representation
- Supervised text classification
- Train/test evaluation
- Dataset abstraction with `fetch_20newsgroups`

## 2. Key Findings

- The initial classifier records approximately **97.24% accuracy** in the stored notebook output.
- Topic separability varies substantially by category pair: hockey versus space reaches about 99%, while Windows X versus computer graphics is harder at about 86%.
- Other stored category comparisons reach roughly 95–96% accuracy.
- These results illustrate a central text-classification idea: categories with more distinctive vocabularies are easier for a bag-of-words Naive Bayes classifier to separate, while closely related technical topics can overlap more strongly.

## 3. How to Run

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install jupyter scikit-learn
jupyter notebook analysis.ipynb
```

The notebook uses `fetch_20newsgroups`; scikit-learn may download the dataset on first use, so internet access can be required.
