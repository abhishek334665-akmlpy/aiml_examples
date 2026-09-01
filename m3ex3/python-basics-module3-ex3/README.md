# Python Basics — Module 3 Exercise 3

A self-contained Jupyter Notebook demonstrating data loading and analysis with the Auto MPG dataset.

## Dataset

This exercise uses the **Auto MPG** dataset from the UCI Machine Learning Repository.

The dataset is **not included in this repository**. Download `auto-mpg.data` from the official UCI dataset page:

https://archive.ics.uci.edu/dataset/9/auto

After downloading, place the file here:

```text
data/auto-mpg.data
```

Create the `data` directory if it does not already exist.

The UCI repository provides the Auto MPG dataset and identifies the dataset as licensed under **Creative Commons Attribution 4.0 International (CC BY 4.0)**. The license permits sharing and adaptation provided appropriate credit is given.

## Dataset Attribution

Quinlan, R. (1993). Auto MPG [Dataset]. UCI Machine Learning Repository.

https://doi.org/10.24432/C5859H

Dataset source:

https://archive.ics.uci.edu/dataset/9/auto

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

```bash
jupyter notebook
```

Open `python_module3_ex3.ipynb` and run the cells.

Make sure `auto-mpg.data` has been downloaded and placed at:

```text
data/auto-mpg.data
```

## Repository Structure

```text
.
├── python_module3_ex3.ipynb
├── data/                  # Create locally after downloading the dataset
│   └── auto-mpg.data     # Not committed to this repository
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

## Public Repository Notes

- The dataset is intentionally excluded from Git and must be downloaded from UCI.
- The official UCI source and required attribution are documented above.
- Notebook outputs and execution counts have been removed.
- Personal names, locations, and environment-specific metadata have been removed.
- No credentials or private paths are included.
