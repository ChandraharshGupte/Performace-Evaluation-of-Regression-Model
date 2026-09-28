# Medical Insurance Cost Prediction using Linear Regression

## Overview

This project develops and evaluates regression models for a real-world application: **Medical Insurance Cost Prediction**.

The project also implements **Gradient Descent from scratch for Linear Regression** and analyzes its convergence and performance.

## Objectives

1. Develop regression models for a real-world application and evaluate their performance using appropriate metrics.
2. Implement and analyze Gradient Descent optimization for Linear Regression.

## Dataset

The project uses a medical insurance dataset containing information such as:

- `age` — age of the policyholder
- `sex` — sex of the policyholder
- `bmi` — body mass index
- `children` — number of children/dependents
- `smoker` — smoking status
- `region` — residential region
- `charges` — medical insurance charges (target variable)

### Data preprocessing

The dataset is cleaned before model training:

- Duplicate records are removed.
- Numerical features are handled separately from categorical features.
- Categorical features (`sex`, `smoker`, and `region`) are converted using One-Hot Encoding.
- Standardization is applied to numerical input features for the Gradient Descent implementation.
- The target variable is `charges`.

Standardization is useful for Gradient Descent because numerical features can have different scales. The `children` feature has a smaller numerical range, so it is standardized along with the other numerical features rather than being treated separately.

## Models

### 1. Standard Linear Regression

Scikit-learn's `LinearRegression` is used as the reference regression model.

### 2. Linear Regression with Gradient Descent

Gradient Descent is implemented manually using:

- Learning rate: `0.03`
- Maximum iterations: `10000`
- Convergence tolerance: `1e-9`

The algorithm:

1. Initializes model parameters.
2. Calculates predictions.
3. Calculates the Mean Squared Error-based cost.
4. Calculates the gradient.
5. Updates the parameters.
6. Repeats until convergence or the maximum number of iterations is reached.

## Evaluation Metrics

The models are evaluated using:

- **R² Score** — measures the proportion of variance in the target explained by the model.
- **MAE (Mean Absolute Error)** — measures the average absolute prediction error.
- **RMSE (Root Mean Squared Error)** — measures the square root of the average squared prediction error.

## Project Files

| File | Description |
|---|---|
| `Medical_Insurance_Regression_Model.ipynb` | Jupyter Notebook containing preprocessing, model training, Gradient Descent, evaluation, and graphs |
| `medical_insurance_cleaned_new.csv` | Cleaned dataset used for the experiment |
| `README.md` | Project documentation |

## Graphs Generated

The notebook generates only the graphs relevant to the assignment:

1. **Actual vs Predicted Medical Insurance Charges**
2. **R² Score Comparison**
3. **Gradient Descent Convergence**

## How to Run

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <YOUR_REPOSITORY_NAME>
```

### 2. Install required libraries

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

### 3. Start Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Medical_Insurance_Regression_Simple.ipynb
```

### 4. Run all cells

Make sure the following file is in the same directory as the notebook:

```text
medical_insurance_cleaned_new.csv
```

## Project Workflow

```text
Load Dataset
     ↓
Remove Duplicate Records
     ↓
Separate Features and Target
     ↓
Train-Test Split
     ↓
Encode Categorical Features
     ↓
Standardize Numerical Features for Gradient Descent
     ↓
Train Standard Linear Regression
     ↓
Implement Gradient Descent
     ↓
Evaluate R², MAE and RMSE
     ↓
Compare Model Performance
     ↓
Analyze Gradient Descent Convergence
```

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Assignment Coverage

This repository directly covers the two required practical objectives:

**1. Regression Model Development and Evaluation**

Medical insurance charges are predicted using Linear Regression and evaluated using R², MAE, and RMSE.

**2. Gradient Descent Implementation and Analysis**

Gradient Descent is implemented from scratch for Linear Regression, and its cost reduction, convergence behavior, and prediction performance are analyzed.

## Notes

The trained model file is not required to run the notebook because the notebook trains the models directly from the cleaned CSV dataset. If a trained model is uploaded separately, it should be treated as an output artifact rather than a required input.

## Author

**Name:** Chandraharsh Gupte
