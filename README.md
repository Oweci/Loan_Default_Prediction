#LoanDefaultPredictionModel

#Problem
Fintech companies need to assess whether a customer is likely to repay a loan. Incorrect decisions can lead to financial losses.

#Objective
Build a machine learning model to predict loan default risk and support better lending decisions.

#Dataset
The dataset contains customer financial and demographic information such as:
- Income
- Employment Type
- Loan Purpose
- Marital Status
- Credit-related features

#Target:
- `Default` (1 = Default, 0 = No Default)

#Approach
1. Data Cleaning
   - Removed ID columns
   - Handled categorical variables using one-hot encoding
2. Handling Imbalance
   - Dataset had ~11% defaulters
   - Used class weighting to improve detection of high-risk customers
3. Model
   - Random Forest Classifier
4. Threshold Tuning
   - Adjusted decision threshold to improve recall for defaulters

#Results
- Accuracy: ~83%
- Recall (Default): improved from 1% → 38%
- Model now identifies significantly more high-risk customers

#BusinessImpact
- Helps identify risky customers before issuing loans
- Reduces financial losses
- Enables risk-based decision making

#FutureImprovements
- Add SMOTE for better imbalance handling
- Deploy as a web app
- Integrate with real-time loan systems
