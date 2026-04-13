# Loan Approval Prediction

A machine learning classification project that predicts loan approval status using exploratory data analysis, feature engineering, and multiple ML algorithms.

## Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [Installation](#installation)
- [Dataset](#dataset)
- [Workflow](#workflow)
- [Results](#results)
- [Usage](#usage)
- [Model Performance](#model-performance)

## Overview

This project builds and evaluates multiple machine learning models to predict whether a loan application will be approved or rejected. The analysis includes comprehensive data exploration, feature engineering, and model comparison to identify the best performing classifier.

**Best Model:** Naive Bayes (highest precision)  
**Runner-up:** Logistic Regression

## Project Structure

```
├── Loan_Approval.ipynb          # Main Jupyter notebook with complete analysis
├── loan_approval_data.csv       # Input dataset (required)
└── README.md                     # This file
```

## Requirements

- Python 3.7+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- jupyter (for running the notebook)

## Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd loan-approval-prediction
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**  
   Or install manually:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn jupyter
   ```

## Dataset

The project uses `loan_approval_data.csv` which should contain loan application data with features such as:
- Applicant demographic information
- Financial metrics
- Loan details
- Approval status (target variable)

**Note:** Ensure the CSV file is in the same directory as the notebook before running.

## Workflow

### 1. **Data Exploration**
   - Load and inspect dataset structure
   - Display basic statistics and data types
   - Identify missing values

### 2. **Data Preprocessing**
   - **Missing Value Handling:**
     - Numerical columns: imputed with mean values
     - Categorical columns: handled appropriately
   - **Data Validation:** verify no missing values remain

### 3. **Exploratory Data Analysis (EDA)**
   - Statistical summaries
   - Distribution analysis
   - Relationship exploration between features
   - Visualization of key patterns

### 4. **Feature Engineering**
   - Categorical encoding (converting text to numerical values)
   - Correlation analysis via heatmap
   - Feature selection optimization

### 5. **Model Development**
   - Train-test split (stratified for class balance)
   - Feature scaling (normalization/standardization)
   - Train multiple models:
     - Naive Bayes
     - Logistic Regression
     - Additional classifiers

### 6. **Model Evaluation & Selection**
   - Precision-based comparison
   - Performance metrics analysis
   - Best model identification

## Results

### Model Performance

| Model | Metric | Status |
|-------|--------|--------|
| **Naive Bayes** | Highest Precision | ⭐ Best Model |
| **Logistic Regression** | Second Best | ⭐⭐ Runner-up |

The analysis identifies **Naive Bayes** as the optimal model based on precision metrics, making it most suitable for minimizing false positives in loan approval predictions.

## Usage

### Running the Complete Analysis

1. **Start Jupyter:**
   ```bash
   jupyter notebook
   ```

2. **Open the notebook:**
   - Navigate to `Loan_Approval.ipynb`
   - Click to open

3. **Execute cells:**
   - Run all cells sequentially using `Cell > Run All`
   - Or run individual cells with `Shift + Enter`

### Making Predictions

After training, you can use the trained model to predict on new data:

```python
# Load trained model and make predictions
new_prediction = model.predict([[features]])
```

## Key Libraries & Functions

- **pandas:** Data manipulation and analysis
- **scikit-learn:** Machine learning models (train_test_split, SimpleImputer, classifiers)
- **numpy:** Numerical computations
- **matplotlib & seaborn:** Data visualization
- **sklearn.impute.SimpleImputer:** Handling missing values
- **sklearn.model_selection:** Train-test splitting and model evaluation

## Notes

- The notebook is self-contained and runs sequentially
- Ensure CSV file is in the working directory
- Feature scaling is applied before model training
- Categorical variables are encoded numerically for model compatibility

## Future Improvements

- Hyperparameter tuning for model optimization
- Cross-validation for robust evaluation
- Additional feature engineering techniques
- Ensemble methods (Random Forest, XGBoost, etc.)
- ROC-AUC and F1-score analysis
- Model deployment pipeline

## Author

Created as a machine learning classification project for loan approval prediction.

## License

This project is open source and available under the MIT License.

---

**Last Updated:** 2026  
**Status:** Complete Analysis ✅
