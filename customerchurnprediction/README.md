# Customer Churn Prediction

## Overview
This project aims to predict customer churn for a subscription-based service using machine learning. The dataset contains customer details, service usage, and churn history. The goal is to develop a model that can identify customers at risk of leaving.

## Dataset
- **Source**: Telco customer churn dataset
- **Size**: 7,043 records
- **Target Variable**: `Churn Label` (Yes/No)
- **Features**: Customer demographics, account information, service subscriptions, and billing details

## Project Steps
1. **Data Collection & Exploration**
   - Loaded dataset from an Excel file
   - Checked missing values, data types, and class imbalance
   - Visualized key trends in tenure, charges, and churn behavior

2. **Feature Engineering**
   - Handled missing values in `Churn Reason`
   - Dropped irrelevant columns (`CustomerID`, `Lat Long`, `Zip Code`, `City`, `State`)
   - Encoded categorical features using Label Encoding and One-Hot Encoding
   - Converted `Total Charges` to numeric and handled missing values
   - Scaled numerical features using Min-Max Scaling

3. **Model Selection & Training** 
   - Split data into training and test sets
   - Train models such as XGBoost
   - Evaluate model performance using accuracy, precision, recall, and F1-score

## How to Run the Project
### Requirements
Ensure you have Python installed and install the necessary dependencies:
```sh
pip install pandas numpy scikit-learn matplotlib seaborn xgboost
```

### Running the Code
1. Load the dataset and preprocess it:
```python
python preprocess.py
```
2. Train the model and evaluate results:
```python
python train_model.py
```

## Future Improvements
- Hyperparameter tuning for better model performance
- Feature selection to reduce dimensionality
- Deployment as an API or web app

## Author
Mavin

---
