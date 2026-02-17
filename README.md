## Raw Dataset
https://www.kaggle.com/datasets/atifmasih/students-drugs-addiction-dataset?resource=download

This dataset contains train and test data seperately which I have combined to form a final raw dataset which is stored in data-raw/

## Deployment Steps
## Phase 1: Data Preprocessing
## Objective

Prepare the raw dataset for machine learning modeling by cleaning, validating, and transforming the data into a model-ready format.

## Preprocessing Steps Performed
# 1. Removed Irrelevant Columns

Dropped S_no (serial number column)

Reason: No predictive value for addiction classification

# 2. Duplicate Removal

Identified 47,968 duplicate rows (~75% of dataset)

Removed duplicates to prevent:

## Model bias

Inflated performance metrics

Data leakage

Dataset reduced from 63,086 to 15,118 rows

# 3. Missing Value Analysis

Identified approximately 12–13% missing values across feature columns

Target variable had no missing values

# 4. Missing Value Treatment

Applied mode imputation for each binary feature column

Justification:

All features are categorical (Yes/No)

Mode preserves original data distribution

Avoids artificial bias that may arise from arbitrary imputation

# 5. Categorical Encoding

Converted Yes to 1

Converted No to 0

Ensured consistent binary representation across all features

# 6. Data Type Standardization

Converted all feature columns to int64

Verified:

No remaining missing values

All features strictly binary (0/1)

# 7. Final Dataset Characteristics

Rows: 15,118

Columns: 11

All features: Binary (0/1)

Target variable: Binary (Addicted / Not Addicted)

No duplicates

No missing values

Fully model-ready dataset

## Outcome

The dataset has been cleaned, validated, and structured for modeling. It is now ready for:

Train-test splitting

Logistic Regression baseline modeling

Probability-based addiction risk scoring
