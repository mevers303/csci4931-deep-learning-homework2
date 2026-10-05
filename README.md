# Deep Learning Homework 2: Customer Churn Prediction

This repository contains the work for CSCI-4931: Deep Learning, Fall 2026.

## Overview

The assignment focuses on predicting customer churn for an European bank using a deep learning model. The dataset contains customer attributes such as credit score, geography, gender, age, tenure, balance, number of products, card ownership, account activity, and salary. The target variable is `Exited`, which indicates whether a customer left the bank.

The goal is to build an artificial neural network (ANN) that learns the relationship between customer features and churn behavior and evaluates its performance using standard classification metrics.

## Repository Contents

- `2026-Fall-DL-hw2.ipynb` — the main Jupyter notebook with the assignment workflow, preprocessing, model training, and evaluation.
- `dataset/` — contains the raw customer churn dataset (`datasetX.csv`).
- `figures/` — image assets used throughout the notebook for documentation and model architecture visualizations.
- `saved_models/` — directory used to store trained model checkpoints.
- `requirements.txt` — Python dependencies required to run the notebook.

## Assignment Tasks

The notebook is organized around the following tasks:

1. Dataset Summary
   - Examine the raw data and summarize key properties.
   - Identify non-numeric columns and missing values.
   - Provide gender- and age-based churn summaries.

2. Data Preprocessing
   - Remove irrelevant or unnecessary columns.
   - Shuffle the data using a fixed random seed.
   - Separate features (`X`) from labels (`y`).
   - Perform an 80/20 train-test split.
   - Apply one-hot encoding to categorical variables such as `Geography` and `Gender`.

3. Neural Network Model 1
   - Train an ANN using the prepared dataset.
   - Evaluate performance on the test set.
   - Report metrics such as accuracy, precision, recall, and F1-score.

4. Neural Network Model 2
   - Repeat the process with a second network architecture.
   - Reuse or adapt the data loader and training pipeline.

5. Neural Network Model 3
   - Repeat the workflow with a third architecture.
   - Compare results across models.

## Dataset Description

The dataset contains both numeric and categorical features, including:

- `CustomerId`
- `Surname`
- `CreditScore`
- `Geography`
- `Gender`
- `Age`
- `Tenure`
- `Balance`
- `NumOfProducts`
- `HasCrCard`
- `IsActiveMember`
- `EstimatedSalary`
- `Exited` (target variable)

The notebook explains that the target column should not be used as an input feature when training the model.

## Setup

To run this project locally:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```

Then open `2026-Fall-DL-hw2.ipynb` in Jupyter.

## Dependencies

The project uses:

- Python
- NumPy
- Pandas
- scikit-learn
- PyTorch

These are listed in `requirements.txt`.

## Notes

- The notebook uses a fixed random seed (`4321`) for reproducibility where stochastic operations are involved.
- One-hot encoding is used instead of label encoding to avoid introducing artificial ordering into categorical variables.
- Trained models are expected to be saved in `saved_models/`.

## License

This repository is provided for coursework use and is not intended as a production package.
