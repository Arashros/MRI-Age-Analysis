# Brain MRI Morphometry and Age Analysis

This project explores how structural brain morphometry features relate to age. It contains a gender-stratified comparison of linear and quadratic fits, plus a PCA-based age prediction exercise.

## Repository layout

- `data/largedataset_clean.txt`: tab-separated source dataset.
- `notebooks/01_gender_stratified_regression.ipynb`: feature-wise regression plots for female and male cohorts.
- `notebooks/02_pca_age_prediction.ipynb`: PCA and regression for age prediction.
- `reports/گزارش-تحلیل-مورفومتری-MRI.docx`: Persian project report; model-result values remain pending notebook execution.

## Setup

Use Python 3. Install dependencies with `python -m pip install -r requirements.txt`, then start Jupyter from the repository root. Open either notebook under `notebooks/`.

The notebook code also looks for the dataset at `../data/` when Jupyter is started from the `notebooks` directory.

## Notes

The repository copy omits the source dataset’s `subejct_label` participant identifier. The notebooks also tolerate its absence. Columns beginning with `lh_` identify left-hemisphere measures and are removed for the right-hemisphere analyses. The regression notebook removes incomplete rows before splitting participants by gender.

The PCA pipeline fits scaling and PCA only on training data and refits them within cross-validation folds. Results are exploratory and should not be interpreted as clinical predictions.
