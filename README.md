## MsDS-customer-churn-prediction
DTSA 5509 Supervised Learning Final Project

## Abstract
I spent 7 years working at Salesforce, one of the largest software as a service (SaaS) companies that sells its cloud software on a subscription based business model. Several of those years were spent in data visualization and business analyst roles working with the renewals organization to build and develop data science models focused on customer health and understand the risk of customers leaving the business.

The main driving focus of these projects was to understand the customer and focus on reducing the chances of customers leaving the subscription based model.  This resulted in a relentless focus on a single KPI, customer attrition (aka customer churn).

In this report, I will play the role of data scientist.  Stepping out of my business-facing role and working with a similar model that was created to predict customer attrition. While I cannot use proprietary business data for this analysis, I will find and use a publicly available customer churn dataset to emulate a similar customer context. I will also use the Random Forest classifier package, similar to the model that was implemented at the company.

## Conclusion
Across the 3 models the 3 performance evaluation scores remained fairly consistent, while the efficiency of the model improved in each iteration through the tuning of hyper-parameters.

Comparing the final model to the baseline model, we saw the following changes in performance scores:

- Mean Accuracy decreased by approximately 0.0 %
- Mean ROC AUC improved by approximately 0.1 %
- F1 Score decreased by approximately 0.0 %

On the whole, these changes to the performance of the model are negligible.

When looking at the efficiency scores, we see significant improvement in how quickly the Random Forest Classifier can execute a train cycle or a score cycle.

Comparing the final model to the baseline model, we saw the following changes in efficiency scores:
- Fit Time improved (decreased) by approximately 59.6 %
- Score Time improved (decreased) by approximately 48.0 %

These changes were obtained by changing the following in the model:
- Reducing the number of estimators from 100 to 35
- Increasing the minimum number of samples in a leaf from 1 to 6
- Caping the max depth of the trees in the forest to 8 levels
- Increasing the number of features allowed in a tree from 6 to 10 features

Summarizing these findings, it can be concluded that through model tuning, the model was able to train and score in half the time at a cost of 0% or less to the performance metrics.

In the scenario outlined, this tradeoff would be viewed as meaningful and we would select the final model to significantly improve efficiency at a small cost to the performance.

## Main Report
The main report is stored in a python notebook under the name [customer_churn_prediction.ipynb](customer_churn_prediction.ipynb)

## Other Useful Content
- **Github Repo Link:** https://github.com/TOM-BOHN/MsDS-customer-churn-prediction
- **[Presentation Slides](https://docs.google.com/presentation/d/1MVGBJoYfayA7F4XZ3TbNTLYXJ-UuapbMyhLUlm4V3Mw/edit?usp=sharing)**
- **[Presentation Video](https://drive.google.com/file/d/15MBnK6NaIbQki00uGUAT-3S8GR7ZqxVE/view?usp=sharing)**
