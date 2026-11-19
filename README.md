# Customer Churn Modelling with scikit-learn

An Ironhack learning project by David Gill exploring how a K-nearest-neighbours classifier can identify customer churn. The customer-retention use case connects data analysis with customer operations.

## Approach

The notebook cleans `TotalCharges`, encodes categorical fields, removes the customer identifier and creates a stratified 80/20 train/test split. It compares several neighbour counts and examines the effect of standardising features.

The recorded conclusion favours K=11 for its balance of recall and accuracy in these experiments. This is an exploratory result rather than an independently validated production model.

## Files

- [SKlearn.ipynb](SKlearn.ipynb): preparation, modelling, metrics and learning notes.
- [WA_Fn-UseC_-Telco-Customer-Churn.csv](WA_Fn-UseC_-Telco-Customer-Churn.csv): the Telco customer-churn dataset used by the notebook.
- [Final_Results_w_Chosen_Model.png](Final_Results_w_Chosen_Model.png): recorded model-results screenshot.
- `.ipynb_checkpoints/`: historical Jupyter checkpoint files.

## Review locally

Install pandas, NumPy, matplotlib, scikit-learn and Jupyter. Open `SKlearn.ipynb` from the repository root so its relative dataset path resolves.

## Evaluation limitations

The notebook compares multiple K values using the test split. A stronger follow-up would choose hyperparameters through cross-validation on the training data, then evaluate once on an untouched holdout set. Recall matters for finding churners, but a business decision also needs the costs of missed churn and unnecessary retention contact.

This project demonstrates a learning workflow. It does not establish performance on an employer's customers. The model has not been retrained or independently benchmarked for this documentation update.
