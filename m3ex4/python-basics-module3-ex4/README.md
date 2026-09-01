# Python Basics — Module 3 Exercise 4

A self-contained Jupyter Notebook demonstrating how to load and inspect the Breast Cancer Wisconsin (Diagnostic) dataset using scikit-learn.

## Dataset

This exercise uses:

```python
from sklearn.datasets import load_breast_cancer

data = load_breast_cancer()
```

The dataset is bundled with scikit-learn's dataset utilities, so **no CSV download is required**. Running `load_breast_cancer()` loads the dataset through scikit-learn.

The dataset contains 569 samples, 30 features, and 2 target classes. Scikit-learn documents it as a copy of the UCI Machine Learning Repository's Breast Cancer Wisconsin (Diagnostic) dataset. citeturn0search0

### Dataset source

- [scikit-learn `load_breast_cancer` documentation](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html)
- [UCI Breast Cancer Wisconsin (Diagnostic) dataset](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic)

The original UCI dataset is licensed under CC BY 4.0. citeturn0search1

## Requirements

- Python 3.10 or newer
- Jupyter Notebook or JupyterLab
- scikit-learn

Install dependencies:

```bash
python -m pip install -r requirements.txt
```

## Run

```bash
jupyter notebook
```

Open `python_module3_ex4.ipynb` and run the cells.

## Repository Structure

```text
.
├── python_module3_ex4.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

## Public Repository Notes

- The dataset is not copied into the repository because scikit-learn provides it through `load_breast_cancer()`.
- No personal information or local environment metadata is included.
- Stored notebook outputs and execution counts have been removed.
