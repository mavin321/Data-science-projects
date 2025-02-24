# Credit Card Fraud Detection

## Overview
This project aims to detect fraudulent credit card transactions using machine learning. The dataset used contains transactions made by European cardholders in September 2013, with highly imbalanced fraud cases.

## Dataset
- **Source:** [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)
- **Size:** 284,807 transactions
- **Fraud cases:** 0.17% of the dataset
- **Features:**
  - `Time`: Seconds elapsed between transactions
  - `Amount`: Transaction amount
  - `V1` to `V28`: Principal components obtained via PCA (to anonymize data)
  - `Class`: Target variable (0 = Legitimate, 1 = Fraudulent)

## Project Steps
### 1. Data Preprocessing
- Handle missing values (if any)
- Normalize the `Amount` and `Time` columns
- Address class imbalance using:
  - Oversampling (SMOTE)
  - Undersampling
  - Class weighting

### 2. Exploratory Data Analysis (EDA)
- Visualize fraud vs. non-fraud distribution
- Correlation heatmap of features
- Boxplots for transaction amounts in fraud vs. non-fraud cases

### 3. Model Selection & Training
- Logistic Regression
- Random Forest
- XGBoost
- Neural Network (Optional)

### 4. Model Evaluation
- Accuracy is not the best metric due to class imbalance
- Use:
  - Precision, Recall, F1-score
  - ROC-AUC Curve

### 5. Hyperparameter Tuning
- Use `GridSearchCV` or `RandomizedSearchCV` to optimize performance

### 6. Deployment (Optional)
- Deploy a fraud detection API using **FastAPI + Docker**
- API accepts transaction data and returns fraud probability

## Installation
### Requirements
- Python 3.x
- NumPy, Pandas, Scikit-learn, XGBoost, Matplotlib, Seaborn
- FastAPI & Uvicorn (for deployment)

### Setup
```bash
# Clone the repository
git https://github.com/mavin321/Data-science-projects.git
cd fraud-detection

# Install dependencies
pip install -r requirements.txt

# Run the training script
python train.py

# (Optional) Start the FastAPI server
uvicorn app:app --reload
```

## Results
- Best-performing model: **XGBoost** (or another model based on evaluation)
- Precision, Recall, and ROC-AUC results displayed in reports

## Contributing
Feel free to open issues or submit PRs to improve the project.



