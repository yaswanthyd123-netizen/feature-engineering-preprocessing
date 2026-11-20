# Preprocessing Design Memo

## Project
RabTech Academy — Task 03: Feature Engineering & Preprocessing Pipeline

## Dataset
`credit-default-risk.csv` is a deterministic synthetic dataset with 1,200 rows. It contains numerical and categorical applicant/loan attributes and a binary `loan_default` target. Missing values are deliberately present in selected input columns to demonstrate imputation.

## Design decisions
1. **Target separation:** `loan_default` is removed from the feature matrix before transformation.
2. **Train/test split first:** an 80/20 stratified split is performed before fitting any imputer, scaler, or encoder.
3. **Numerical preprocessing:** median imputation is robust to skewed values; `StandardScaler` standardizes numeric columns.
4. **Categorical preprocessing:** most-frequent imputation is followed by `OneHotEncoder(handle_unknown="ignore")`.
5. **Reusable pipeline:** `ColumnTransformer` combines both branches and is placed inside a Scikit-Learn `Pipeline` with a Random Forest classifier.
6. **Feature analysis:** mutual information is computed using training data; permutation importance is computed against the held-out test set.

## Leakage prevention
All learned preprocessing parameters are fitted only during `model_pipeline.fit(X_train, y_train)`. The test set is transformed by the already-fitted pipeline and is not used to learn imputation statistics, scaling parameters, or category vocabulary.

## Expected proof
The Jupyter notebook contains the code, execution-ready workflow, evaluation metrics, and feature-importance analysis.
