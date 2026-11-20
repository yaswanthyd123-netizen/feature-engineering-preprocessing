# Feature Engineering & Preprocessing Pipeline

**RabTech Academy — Task 03**

A reusable, leakage-aware machine-learning preprocessing workflow using Python, Pandas, and Scikit-Learn.

## Files
- `feature_engineering_pipeline.ipynb` — complete Jupyter Notebook implementation.
- `credit-default-risk.csv` — synthetic tabular dataset (1,200 rows).
- `preprocessing_design_memo.md` — design choices and leakage prevention.
- `responsible_data_card.md` — dataset purpose, composition, and limitations.
- `responsible_data_card.html` — HTML version of the data card.
- `risk_register.md` — key implementation and responsible-use risks.

## Requirements
- Python 3.9+
- pandas
- numpy
- matplotlib
- scikit-learn
- jupyter
- notebook

Install dependencies:

```bash
python -m pip install pandas numpy matplotlib scikit-learn jupyter notebook
```

## Run
1. Keep the notebook and CSV file in the same folder.
2. Open the folder in VS Code or Jupyter Notebook.
3. Open `feature_engineering_pipeline.ipynb`.
4. Run all cells from top to bottom.

## Workflow
1. Load and inspect the data.
2. Separate features and target.
3. Split into training and testing sets before preprocessing.
4. Build numerical and categorical preprocessing pipelines.
5. Train a Random Forest model.
6. Evaluate on held-out test data.
7. Review mutual-information and permutation feature importance.

## Leakage prevention
Imputers, scaler, and encoder are fitted as part of the Scikit-Learn pipeline on training data only. The test set is held out for evaluation.

## Dataset disclaimer
The included credit-default dataset is synthetic and intended only for educational demonstrations. It must not be used for real lending or other consequential decisions.
