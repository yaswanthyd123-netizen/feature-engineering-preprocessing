# Responsible Data Card

## Dataset name
Synthetic Credit Default Risk Dataset

## Purpose
Educational demonstration of missing-value imputation, scaling, categorical encoding, train/test separation, and feature-importance analysis.

## Composition
- 1,200 synthetic rows.
- Numerical features: age, annual income, loan amount, credit score, employment years, debt-to-income ratio, and loan term.
- Categorical features: education, employment type, home ownership, and loan purpose.
- Target: `loan_default` (0 or 1).
- Missing values are included in selected input features.

## Source and privacy
Generated programmatically for this learning task. It does not contain real people, customer records, or personally identifiable information.

## Appropriate use
Use only for learning and testing code. Do not use the data or resulting model to approve/deny credit, price loans, or make decisions about real people.

## Limitations and risks
Synthetic patterns do not represent the complexity of real lending data. Feature relationships and model scores are illustrative. A real deployment would require data provenance review, legal and privacy review, representative validation, subgroup performance and fairness testing, explainability, monitoring, and human governance.
