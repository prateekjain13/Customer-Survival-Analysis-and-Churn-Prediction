# Customer Survival Analysis and Churn Prediction

Customer attrition, also known as customer churn, customer turnover, or customer defection, is the loss of clients or customers.

Telephone service companies, Internet service providers, pay TV companies, insurance firms, and alarm monitoring services, often use customer attrition analysis and customer attrition rates as one of their key business metrics because the cost of retaining an existing customer is far less than acquiring a new one. Companies from these sectors often have customer service branches which attempt to win back defecting clients, because recovered long-term customers can be worth much more to a company than newly recruited clients.

Predictive analytics use churn prediction models that predict customer churn by assessing their propensity of risk to churn. Since these models generate a small prioritized list of potential defectors, they are effective at focusing customer retention marketing programs on the subset of the customer base who are most vulnerable to churn.

In this project I aim to perform customer survival analysis and build a model which can predict customer churn. I also aim to build an app which can be used to understand why a specific customer would stop the service and to know his/her expected lifetime value.

## Final Customer Churn Prediction App

<img src=https://github.com/archd3sai/Customer-Survival-Analysis-and-Churn-Prediction/blob/master/app-pic.png>

## Customer Survival Analysis

**Survival Analysis:**
Survival analysis is generally defined as a set of methods for analyzing data where the outcome variable is the time until the occurrence of an event of interest. The event can be death, occurrence of a disease, marriage, divorce, etc. The time to event or survival time can be measured in days, weeks, years, etc.

For example, if the event of interest is heart attack, then the survival time can be the time in years until a person develops a heart attack.

**Objective:**
The objective of this analysis is to utilize non-parametric and semi-parametric methods of survival analysis to answer the following questions.

- How the likelihood of the customer churn changes over time?
- How we can model the relationship between customer churn, time, and other customer characteristics?
- What are the significant factors that drive customer churn?
- What is the survival and Hazard curve of a specific customer?
- What is the expected lifetime value of a customer?

**Customer Lifetime Value:**

To calculate customer lifetime value, I would multiply the Monthly charges the customer is paying to Telcom and the expected life time of the customer.

I utilize the survival function of a customer to calculate its expected life time. I would like to be little bit conservative and consider the customer is churned when the survival probability of him is 10%.

## Customer Churn Prediction

I aim to implement a machine learning model to accurately predict if the customer will churn or not.

## Flask App

I saved the final tuned Random Forest model and deployed it using Flask web app. Flask is a micro web framework written in Python. It is designed to make getting started quick and easy, with the ability to scale up to complex applications. I saved the shap value explainer tuned using random forest model to show shap plots in app. I have also utilized the cox-proportional hazard model to show survival curve and hazard curve, and to calculate expected customer lifetime value.

The final app shows churning probability, gauge chart of how severe a customer is and shap values based on customer's data. The final app layout can be seen above.
