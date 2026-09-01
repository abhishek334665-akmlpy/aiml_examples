# Module 3 — Wine Quality Regression

A Jupyter Notebook demonstrating regression analysis using the UCI Wine Quality dataset.

## Dataset

This exercise uses the **Wine Quality** dataset from the UCI Machine Learning Repository.

The dataset is **not included in this repository**. Download `winequality-red.csv` from the official UCI dataset page:

https://archive.ics.uci.edu/dataset/186/wine+quality

For this notebook, download the red-wine dataset file and place it at:

```text
data/winequality-red.csv
```

Create the `data` directory locally if needed.

### Dataset Attribution

Cortez, P., Cerdeira, A., Almeida, F., Matos, T., & Reis, J. (2009). *Wine Quality* [Dataset]. UCI Machine Learning Repository.

https://doi.org/10.24432/C56S3T

The UCI Machine Learning Repository lists the Wine Quality dataset under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license. The license permits sharing and adaptation provided appropriate credit is given.

## Requirements

- Python 3.10+
- Jupyter Notebook or JupyterLab
- NumPy
- pandas
- Matplotlib
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

Open `Module3_Wine_Quality_Regression.ipynb`.

Before running the notebook, make sure the dataset exists at:

```text
data/winequality-red.csv
```

## Repository Structure

```text
.
├── Module3_Wine_Quality_Regression.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

The `data/` directory is intentionally not committed. Download the dataset separately from the official UCI source.

## Public Repository Notes

- No personal information or local machine paths are included.
- Notebook outputs and execution counts have been removed.
- The external dataset is documented with its official source, citation, DOI, and license.
