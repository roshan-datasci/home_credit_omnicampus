# Home Credit Default Risk Prediction

## Overview
This project explores a binary classification problem: predict the probability of loan repayment difficulty (`TARGET = 1`) using applicant data.

## Notebook
Open `home_credit_default_risk.ipynb` in Google Colab or Jupyter. The notebook:
- loads the competition train/test CSVs,
- checks target distribution and missing values,
- preprocesses numeric and categorical features in a leakage-conscious pipeline,
- evaluates a Logistic Regression baseline using validation ROC-AUC,
- optionally compares LightGBM,
- trains the selected model on all training rows and writes `submission.csv`.

## Data
The competition dataset is not included in this repository. Obtain it through the authorized competition/course page and follow its terms. In Colab, upload CSV files named like `train.csv` and `test.csv` when prompted.

## Run
1. Open the notebook in Google Colab.
2. Run cells from top to bottom.
3. Upload the train and test CSV files when prompted.
4. Read the validation ROC-AUC printed by the notebook.
5. The notebook creates and downloads `submission.csv`.

Optional LightGBM comparison: in a Colab code cell run `!pip install lightgbm`, rerun the LightGBM cell, and set `USE_LIGHTGBM = True` only if its validation score is better.

## Results
Previously reported by the project owner:
- Logistic Regression validation ROC-AUC: approximately **0.73078**
- Competition public score: approximately **0.73886**

These are historical results from the earlier starter notebook/submission, not results from a fresh run of this revised notebook. Re-run the notebook to verify the current results.

## Limitations
This is a learning project and baseline, not a production credit-risk model. Results depend on the data, validation split, and environment. No guarantee of improved leaderboard performance is made.

## Suggested next steps
- Add cross-validation.
- Experiment with domain-informed features.
- Compare several models with the same validation strategy.
- Document experiments and reproducibility.
