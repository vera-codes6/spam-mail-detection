# Email Spam Detection (Machine Learning)

A simple machine-learning workflow to detect spam messages from text. The project is delivered as a reproducible Jupyter Notebook and a CSV dataset.

This repository is part of an Oasis Infobyte internship task focused on classical NLP for spam detection.

## Repository contents

- `Email_Spam_Detection_with_Machine_Learning.ipynb` — end-to-end notebook: EDA, preprocessing, feature extraction, model training, and evaluation.
- `spam.csv` — dataset used by the notebook.
- `README.md` — this file.

## Dataset

- The notebook expects `spam.csv` in the project root.
- The file contains labeled text messages for binary classification (ham vs spam).
- If you use a different dataset or path, update the corresponding cell in the notebook where the CSV is loaded.

## Approach

The notebook demonstrates a typical text-classification pipeline:

- Exploratory data analysis (class balance, message length, frequent terms)
- Text preprocessing (lowercasing, punctuation removal, optional stopword removal, tokenization)
- Feature extraction with Bag-of-Words and/or TF–IDF
- Model training with classical algorithms (e.g., Multinomial Naive Bayes, Logistic Regression, SVM)
- Evaluation using accuracy, precision, recall, F1-score, and confusion matrix

## Quick start (Windows, PowerShell)

Prerequisites:

- Python 3.8+ installed and available on PATH
- Internet access to install Python packages

Setup steps:

1) Create and activate a virtual environment

```
python -m venv .venv
.\.venv\Scripts\Activate
```

2) Install the core dependencies

```
python -m pip install --upgrade pip
pip install jupyter pandas numpy scikit-learn matplotlib seaborn nltk
```

3) (Optional) Download NLTK resources if the notebook uses them

```
python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords')"
```

4) Launch Jupyter and run the notebook

```
jupyter notebook
```

Open `Email_Spam_Detection_with_Machine_Learning.ipynb` and run the cells top to bottom. Ensure `spam.csv` is present at the repository root before executing the data-loading cell.

## Results

The notebook reports standard classification metrics and visualizations to compare models. Use these outputs to select the best-performing model for your use case.

## Reproducibility

- A single, self-contained notebook ensures the full pipeline is visible and repeatable.
- For consistent runs, set random seeds where applicable and keep the same library versions.

## Notes

- This project is intended for educational purposes and as a starting point for production systems.
- For deployment, consider model persistence (e.g., `pickle`/`joblib`), input validation, and continuous monitoring.

## Acknowledgments

- Oasis Infobyte — internship task inspiration
