# credit-risk-classification
Analysis Report:

The purpose of this analysis is to build a logistic regression model that predicts the likelihood of a loan defaulting, classified as high-risk (1) or healthy (0). By analyzing the historical loan data, the model aims to determine which factors are most indicative of default risk. 

Model Performance:
- Accuracy: 
    - 62%. This means that the model correctly predicted whether a loan was healthy or high-risk 62% of the time.
- Precision:
    - For healthy loans (label 0), the precision is 1.00, meaning that when the model predicts a healthy loan, it is almost always correct.
    - For high-risk loans (label 1), the precision is 0.08, indicating that the model struggles significantly to correctly identify high-risk loans.
- Recall:
    - For healthy loans (label 0), the recall is 0.60, meaning that the model correctly identifies 60% of the actual healthy loans.
    - For high-risk loans (label 1), the recall is 1.00, meaning that the model successfully identifies all high-risk loans, but given the low precision, it often misclassifies healthy loans as high-risk.

Summary:
The logistic regression model demonstrates an overall accuracy of 62%, which might seem reasonable at first glance. However, upon closer inspection, it becomes clear that the model is heavily biased toward predicting healthy loans correctly, as evidenced by its perfect precision for healthy loans (1.00). Unfortunately, this comes at the expense of misclassifying many healthy loans as high-risk (low precision for high-risk loans at 0.08).

The perfect recall for high-risk loans (1.00) shows that the model catches every high-risk loan, but its low precision suggests a high false positive rate for predicting high-risk loans. This means that the model flags many healthy loans as risky.

Recommendation: I would not recommend deploying this model in its current state due to the severe imbalance in precision and recall for predicting high-risk loans. The model may lead to too many false positives, flagging healthy loans as risky. To improve this, adjustments such as balancing the dataset, exploring alternative machine learning models, or tuning hyperparameters could be necessary.