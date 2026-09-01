# Bank Marketing Analysis

A self-contained Jupyter Notebook demonstrating data loading, exploratory analysis, preprocessing, and binary classification using the UCI Bank Marketing dataset.

## Dataset

This notebook expects the following file:

```text
data/bank-full.csv
```

The dataset is **not included in this repository**. Download it from the official UCI Machine Learning Repository:

- UCI Bank Marketing dataset: https://archive.ics.uci.edu/dataset/222/bank+marketing

After downloading the dataset, extract `bank-full.csv` into the `data/` directory.

The UCI repository identifies this as the Bank Marketing dataset and provides `bank-full.csv` as the full dataset with 17 inputs. The dataset is licensed under **CC BY 4.0**. Please retain the appropriate attribution when redistributing or using the dataset. 

## Requirements

- Python 3.10 or newer
- Jupyter Notebook or JupyterLab
- pandas
- matplotlib
- scikit-learn

Install dependencies:

```bash
python -m pip install -r requirements.txt
```

## Run

From the repository root:

```bash
jupyter notebook
```

Open `python_module5.ipynb` and run the cells.

The notebook reads the dataset using:

```python
pd.read_csv("data/bank-full.csv", sep=";")
```

Therefore, keep the downloaded CSV at exactly:

```text
data/bank-full.csv
```

## Repository Structure

```text
.
├── python_module5.ipynb
├── data/
│   └── .gitkeep
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

## Data Policy

The dataset is intentionally excluded from this repository. Users should download it directly from the official UCI source and place it under `data/`.

## Dataset Citation

Moro, S., Rita, P., & Cortez, P. (2014). Bank Marketing [Dataset]. UCI Machine Learning Repository. DOI: 10.24432/C5K306.
