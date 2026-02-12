
# Polynomial Regression (Jupyter Notebook)

This repo contains a Jupyter notebook: `polynomial-regression.ipynb`, that trains and visualizes a Polynomial Regression model (built using Linear Regression on polynomial features) with scikit-learn.

## What the notebook does
- Loads the **Position_Salaries.csv** dataset
- Sets:
  - `X` = position level (feature)
  - `y` = salary (target)
- Trains a baseline **Linear Regression** model for comparison
- Creates polynomial features with `PolynomialFeatures(degree=4)`
- Trains a second Linear Regression model on the transformed polynomial features
- Plots:
  - Linear Regression fit vs data
  - Polynomial Regression fit vs data
- Predicts the salary for a sample input level **6.5** using both models

## Dataset
The notebook expects a CSV like `Position_Salaries.csv` with columns similar to:
- Position
- Level
- Salary

In the notebook, the dataset path is set to:
`/kaggle/input/polynomial/Position_Salaries.csv`

If you are not running on Kaggle, update that path to wherever your CSV lives.

## Requirements
- Python 3.x
- numpy
- pandas
- matplotlib
- scikit-learn

Install deps:
```bash
pip install numpy pandas matplotlib scikit-learn
```

## How to run locally
1. Put `Position_Salaries.csv` next to the notebook (or anywhere you like).
2. Update the dataset path in the notebook:

```python
dataset = pd.read_csv("Position_Salaries.csv")  # or your local path
```

3. Run all cells.

## Output
- Two plots (linear fit and polynomial fit)
- Two predictions for `[[6.5]]`:
  - One from the linear model
  - One from the polynomial model (degree 4)

## Notes and common issues
- File not found errors are almost always due to the CSV path. Change it to a valid local path.
- `degree=4` controls the curve complexity. Higher degrees can fit the training data more closely but may overfit.
