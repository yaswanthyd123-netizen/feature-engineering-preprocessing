# Risk Register — Feature Engineering & Preprocessing

| Risk | Why it matters | Mitigation in this task |
|---|---|---|
| Data leakage | Test information can inflate evaluation results. | Split first; fit preprocessing only through the training pipeline. |
| Missing values | Many estimators cannot handle missing values directly. | Median imputation for numerical fields; most-frequent imputation for categorical fields. |
| Unseen categories | New categories can break inference. | OneHotEncoder uses `handle_unknown="ignore"`. |
| Feature scale differences | Numeric ranges can differ substantially. | StandardScaler is applied to numerical features. |
| Imbalanced target | Accuracy alone may hide poor minority-class performance. | Stratified split; report precision, recall, F1, and ROC-AUC alongside accuracy. |
| Misleading feature importance | Importance is not causation and can vary across samples. | Describe MI and permutation importance as exploratory diagnostics. |
| Synthetic-data overclaim | Synthetic results do not establish real-world performance. | Clearly label dataset and results as educational only; prohibit real lending use. |
