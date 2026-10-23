# Naive Bayes Email Classifier

**Historical machine learning project (2019)** — a desktop spam/ham email classifier using **bag-of-words features and multinomial Naive Bayes**.

> This is an archived-in-practice learning project, not an actively maintained spam-filter product. The original code relies on older Python and pandas conventions. The repository is kept as evidence of early ML experimentation, not as a production-ready or benchmarked classifier.

## What the code contains

- **Dataset loading:** reads message bodies from local `hams/` and `spams/` directories. Separate `hams_t/` and `spams_t/` directories are used for test examples.
- **Feature engineering:** `sklearn.feature_extraction.text.CountVectorizer` turns email text into a bag-of-words feature matrix.
- **Classification:** `sklearn.naive_bayes.MultinomialNB` trains on the labelled spam/ham examples.
- **Evaluation:** the original script computes true positives, true negatives, false positives and false negatives, displays a confusion matrix and simple classification statistics.
- **User interface:** `app_final.py` provides a Tkinter-based desktop form.

```text
spam / ham messages
         │
         ▼
   CountVectorizer
         │
         ▼
    MultinomialNB
         │
         ▼
    spam / ham label
```

## Important reproducibility limitations

- Some code uses Python 2 syntax, including `Tkinter` and iterator conventions.
- Deprecated pandas methods such as `DataFrame.append` are present.
- Some GUI/evaluation routines need fixes before a current Python 3 run.
- There are **no independently validated precision/recall numbers** claimed in this README.

For the current applied-ML direction, see the [Production ML Pipeline roadmap](https://omaroid.github.io/roadmap/) covering leakage checks, measured evaluation, calibration, serving and drift.

**Author's portfolio:** [Omar Laraqui](https://omaroid.github.io/) · [Selected work](https://omaroid.github.io/#work)
