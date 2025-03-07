# SyriaTel Customer Churn Prediction

## Business Understanding
SyriaTel, a telecom provider, faces a customer retention challenge. Churn prediction is crucial, as retaining existing customers is often more cost-effective than acquiring new ones. The goal is to build a classifier to predict if a customer will "soon" leave SyriaTel.

## Problem Statement
The main objective is to create a predictive model that accurately identifies customers at risk of churning. By analyzing historical data on service usage, billing details, and customer interactions, the project aims to uncover patterns linked to churn. This insight will help SyriaTel implement targeted retention strategies, such as personalized promotions or improved customer service.

## Project Objectives
1. Develop a binary classification model to predict customer churn.
2. Identify key features that influence churn.
3. Enhance predictive accuracy through preprocessing and feature selection.
4. Optimize model performance with feature engineering and tuning.
5. Evaluate churn prediction using metrics like accuracy and recall.

## Success Criteria
- Achieve at least 85% accuracy and recall in churn prediction.
- Minimize false positives to reduce unnecessary retention costs.
## Model Evaluation
The metrics for evaluation that I focussed on with modelling is Accuracy and Recall.Recall is beneficial to the business since we are focusing on client retention.The best performing model is Random Forest with a Recall of 99.82% and accuracy of 94.63% Since we are foccused on predicting churn and customer retention.Which is can be seen with the output below.
## Model Performance Summary
### Logistic Regression
- Untuned:
  - Accuracy: 89.90%
  - Recall: 97.98%
  - F1 Score: 94.51%
- Tuned:
  - Accuracy: 78.99%
  - Recall: 78.35%
  - F1 Score: 86.88%

### Decision Tree
- Untuned:
  - Accuracy: 92.02%
  - Recall: 95.05%
  - F1 Score: 95.48%
- Tuned:
  - Accuracy: 93.32%
  - Recall: 96.70%
  - F1 Score: 96.26%

### Random Forest
- Untuned:
  - Accuracy: 94.79%
  - Recall: 99.63%
  - F1 Score: 97.14%
- Tuned:
  - Accuracy: 94.63%
  - Recall: 99.82%
  - F1 Score: 97.06%

## Conclusion
Model Performance

The Random Forest model outperformed the other models, achieving a recall of 99.63% and an accuracy of 94.79% before tuning. After tuning, the recall remained strong, indicating its robustness in identifying churn cases accurately.The Decision Tree model also performed well, especially after tuning, with a recall of 96.7% and an accuracy of 93.32%.The Logistic Regression model, while offering insights into feature importance, showed slightly lower performance compared to tree-based models. The recall decreased to 97.06% after tuning, with an accuracy of 90.39%.

Feature Importance

The top features influencing churn varied across models: Logistic Regression: International plan, voicemail plan, and total day plan were significant. Decision Tree: Total day minutes, total international calls, and total international charge were prominent. Random Forest: Further validated the importance of these features, emphasizing total usage metrics and international service plans.

The major impact of the International Plan feature across all models indicates that customers with this plan are more likely to churn. This raises the possibility of a pricing or value perception conflict. Another important component of the Logistic Regression model was the Voicemail Plan. This plan may not be valuable to customers, which would increase churn.

Patterns of Call Usage:

Two powerful indicators of churn are total international calls and total day minutes. High usage in these locations could be a sign that a better plan is needed or that call quality and pricing aren't meeting your needs.
## Recommendations
1. Use the International Plan to develop exclusive deals or customer retention tactics. This could include better-value combined deals, discounts, or promotions. To better serve clients with high daytime usage and lower churn risk, create individualized strategies for them.

2. Strategies for Preventing Churn: For high-risk clients, put in place a proactive customer interaction program. When usage patterns resemble those of likely churners, for instance, offers may be sent or satisfaction surveys may be carried out

3.  Deployment of the Model: For production use, implement the Random Forest model since it provides the optimal balance between recall and accuracy, guaranteeing a low number of false negatives in churn prediction.

4.  Observation and Iteration: To maintain accuracy, keep an eye on the model's performance at all times and retrain it occasionally using new data. Create feature drift notifications, particularly if usage trends change over time.

