# Machine Learning Project for Credit Default Prediction

## What is this project?

This is a **machine learning project** that predicts credit card default risk using customer demographic and payment history data. The project implements a **Random Forest Classifier** to determine whether a customer is likely to default on their credit card payment next month.

## Dataset

The project uses the **Credit Card Default Dataset** (`credit_card_default.csv`) which contains:
- **30,000 credit card customer records**
- **24 features** including:
  - Demographic information (age, sex, education, marriage status)
  - Credit limit and payment history
  - Bill amounts and payment amounts for 6 months
- **Target variable**: `default_payment_next_month` (1 = default, 0 = no default)

### Key Features:
- `LIMIT_BAL`: Credit limit
- `SEX`: Gender (1=male, 2=female)
- `EDUCATION`: Education level
- `MARRIAGE`: Marital status
- `AGE`: Age of customer
- `PAY_0` to `PAY_6`: Payment status for past 6 months
- `BILL_AMT1` to `BILL_AMT6`: Bill amounts for past 6 months
- `PAY_AMT1` to `PAY_AMT6`: Payment amounts for past 6 months

## Project Files

| File | Description |
|------|-------------|
| `Default_preprocessed.ipynb` | Main notebook with complete ML pipeline including data exploration, preprocessing, model training, and evaluation |
| `postpre.ipynb` | Additional notebook with preprocessing and analysis |
| `credit_card_default.csv` | The dataset containing credit card customer information |

## Methodology

### 1. Data Understanding & Exploration
- Comprehensive analysis of customer demographics
- Investigation of payment patterns and bill amounts
- Identification of potential biases (especially in marital status representation)

### 2. Data Preprocessing
- Missing value handling (dropping minimal missing values)
- Feature scaling and normalization
- Data type conversions and cleaning

### 3. Machine Learning Model
- **Algorithm**: Random Forest Classifier
- **Reason**: Handles mixed data types well, provides feature importance, robust to outliers
- **Configuration**: `RandomForestClassifier(random_state=42)` for reproducibility

### 4. Model Evaluation
- **Accuracy**: **82.04%**
- The model correctly predicts credit default risk in approximately 82 out of 100 cases

## Key Findings

1. **Model Performance**: Achieved 82.04% accuracy in predicting credit card defaults
2. **Bias Analysis**: Identified potential representation bias in marital status data
3. **Feature Importance**: Payment history and bill amounts are likely key predictors
4. **Data Quality**: Minimal missing values, well-structured dataset

## Potential Applications

- **Risk Assessment**: Banks can use this model to evaluate loan/credit applications
- **Portfolio Management**: Financial institutions can identify high-risk customers
- **Preventive Measures**: Early intervention for customers showing default patterns
- **Regulatory Compliance**: Supporting fair lending practices with bias analysis

## Technical Requirements

- Python 3.x
- Pandas for data manipulation
- Scikit-learn for machine learning
- Jupyter Notebook environment

## Usage

1. Open either notebook (`Default_preprocessed.ipynb` or `postpre.ipynb`) in Jupyter
2. Ensure the `credit_card_default.csv` file is in the same directory
3. Run all cells to reproduce the analysis and model training
4. The trained model can make predictions on new customer data

## Model Limitations

- Accuracy of 82.04% means ~18% of predictions may be incorrect
- Potential bias in marital status representation needs consideration
- Model trained on specific demographic and temporal data
- Results should be validated with additional recent data

---

**Note**: This project demonstrates end-to-end machine learning workflow from data exploration to model deployment for credit risk assessment in the financial domain.