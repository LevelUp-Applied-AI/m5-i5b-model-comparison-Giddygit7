# Tree vs. Linear Disagreement Analysis

## Sample Details

- **Test-set index:** 777
- **True label:** 0
- **RF predicted P(churn=1):** 0.5998
- **LR predicted P(churn=1):** 0.1700
- **Probability difference:** 0.4299

## Feature Values

- **tenure:** 36.0
- **monthly_charges:** 20.0
- **total_charges:** 1077.33
- **num_support_calls:** 2.0
- **senior_citizen:** 0.0
- **has_partner:** 0.0
- **has_dependents:** 0.0
- **contract_months:** 1.0

## Structural Explanation

The models disagree here because the Random Forest is likely capturing a non-linear interaction or a threshold effect that the Logistic Regression cannot represent. While LR is forced to treat each feature as having a constant global relationship with churn (e.g., higher charges always increases risk by a fixed amount), the RF can identify that a specific combination of features—such as high monthly_charges paired specifically with low tenure—creates a high-risk pocket that doesn't follow the general linear trend of the rest of the dataset.
