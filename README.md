# Fake Job Posting Detection — Master's Project Review Package

## Overview
The original student project compares TF-IDF text classification (including Logistic Regression and XGBoost) with an LSTM/GloVe approach for detecting fraudulent job postings. Original notebook outputs are historical, **not independently verified**.

## Contents
- `original_notebooks/`: original submitted preprocessing and modeling notebooks, retained without methodological edits.
- `review_baseline.ipynb`: a newly prepared leakage-safe Logistic Regression baseline.
- `data/fake_job_postings_sample.csv`: 850-row stratified demonstration subset (700 real, 150 fraudulent); deliberately not representative of the original class prevalence.
- `requirements.txt`: minimal dependencies for the review baseline. Original LSTM/XGBoost experiments need additional packages and GloVe data.

## Run
1. Install Python 3.10+ and `pip install -r requirements.txt`.
2. Open `review_baseline.ipynb` in Jupyter and run all cells.
3. For full-dataset research, replace the sample with the original data and rerun with properly isolated splits and validation.

## Important limitations
- The baseline notebook has not been executed or benchmarked as part of this package.
- Original notebook modeling fits TF-IDF before splitting, which can leak test-set distribution information. The original LSTM threshold should be selected on validation data rather than test results.
- The original notebooks require their original datasets, dependencies, and embeddings to fully reproduce.
- Dataset is for educational review; inspect licensing and privacy before redistribution.
- Authorship and individual contributions should be described accurately when sharing group work.
