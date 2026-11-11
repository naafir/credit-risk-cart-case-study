# Credit Risk Analysis with CART (German Credit Dataset)

Case study for Modules III and IV by **Muhammad Naafir A**, B.Tech CSE, B.S. Abdur Rahman Crescent Institute of Science and Technology.

## What this project does
Using the Statlog German Credit dataset (1,000 loan applicants, 20 attributes), the notebook covers:

1. Retrieving and importing the dataset (frozen as `credit_g_frozen.csv`)
2. Data preparation: index field and changed field values
3. Identifying and handling categorical data (one-hot encoding)
4. Re-expression (log transform of skewed fields)
5. Standardising numeric data (z-scores)
6. Identifying and handling outliers (|z| > 3, capping)
7. Partitioning into training (70%) and testing (30%) sets, stratified
8. Validating the partition (chi-square, t-tests) and balancing the training set
9. Building a CART classification tree (credit risk) and a CART regression tree (loan amount)
10. Evaluating the models

## Key results (test set)
| Model | Result |
|---|---|
| Classification tree | Accuracy 0.653, recall (bad risk) 0.567, F1 0.495, ROC-AUC 0.679 |
| Regression tree (log loan amount) | R2 0.511, MAE 0.417, RMSE 0.552 |

## Files
- `CART_Credit_Risk_Case_Study.ipynb` - the full notebook (run top to bottom)
- `credit_g_frozen.csv` - the frozen dataset used for the presentation
- `CART_Credit_Risk_Report.pdf` - the written report

## How to run
Open the notebook in Google Colab, upload `credit_g_frozen.csv` to the Colab files panel (or let the notebook download it), and choose Runtime > Run all. All random steps use `random_state = 42`, so results are reproducible.
