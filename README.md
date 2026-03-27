#AI-Powered Loan Default Risk Prediction System
Project Highlights

- Built a loan default prediction model using real-world data
- Handled class imbalance (11% defaulters)
- Improved recall from **1% → 38%**
- Implemented **risk scoring system**
- Applied **threshold tuning for business impact**
## Problem

Loan default prediction is critical for financial institutions because it directly impacts risk management, loan approval decisions, and profitability.

##Objective

Build a machine learning model to predict whether a customer will default on a loan and create a risk scoring system to support decision-making.

##Dataset

The dataset includes:

* Customer demographics (Education, Marital Status)
* Financial information
* Loan-related features

Target:

**Default (1 = Default, 0 = No Default)**

## Approach

### 1. Data Preprocessing

* Dropped unnecessary ID column (LoanID)
* Converted categorical variables using one-hot encoding

### 2. Handling Class Imbalance

* Dataset had only **~11% defaulters**
* Used `class_weight='balanced'` to improve model focus on minority class

### 3. Model Used

* Random Forest Classifier

### 4. Model Improvement (KEY STEP)

* Initial model had very low recall for defaulters (~1%)
* Applied **threshold tuning (0.5 → 0.2)**
* Improved ability to detect high-risk customers

## Results

| Metric              | Value                      |
| ------------------- | -------------------------- |
| Accuracy            | ~83%                       |
| Recall (Default)    | **Improved from 1% → 38%** |
| Precision (Default) | ~32%                       |

The model now captures significantly more defaulters, making it useful for real-world applications.

## Risk Scoring System

Instead of only predicting default, the model outputs a **probability score**:

Example:

* 0.10 → Low risk
* 0.40 → Medium risk
* 0.80 → High risk

### Decision Rules:

* **0.0 – 0.2 → Approve**
* **0.2 – 0.5 → Review**
* **0.5+ → Reject**

## Business Impact

* Helps fintech companies identify high-risk customers
* Reduces financial losses from loan defaults
* Enables smarter, data-driven lending decisions

## Future Improvements

* Apply SMOTE for better balancing
* Try advanced models (XGBoost, LightGBM)
* Deploy as a web application (Streamlit)
* Add explainability (feature importance)


## Note

The trained model file is not included due to size limitations.
To reproduce results, run the notebook provided.
