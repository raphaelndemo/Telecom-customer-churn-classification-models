# Customer Churn Prediction

A machine learning project focused on predicting customer churn using object-oriented programming principles with telecom customer data from BigML.

## Project Overview

Customer churn is a major challenge for telecommunications companies, as losing customers directly reduces recurring revenue and increases acquisition costs. Retaining existing customers is generally more cost-effective than acquiring new ones.

This project analyzes customer data to predict whether a customer is likely to churn (leave the service). It uses telecom customer information—including call patterns, service plans, and account details—to build interpretable classification models that can support proactive, data-driven retention strategies.

The goal of this project is not only to predict churn, but also to understand the key behavioral factors associated with customer attrition so that business stakeholders can take informed action.

## Dataset

**File:** `Data/bigml_59c28831336c6604c800002a.csv`

The dataset contains approximately 3,335 customer records with the following features:

### Customer Information
- **state**: Customer's state code
- **account length**: Number of days the account has been active
- **area code**: Telephone area code
- **phone number**: Customer's phone number (identifier)

### Service Features
- **international plan**: Whether the customer has an international plan (yes/no)
- **voice mail plan**: Whether the customer has a voice mail plan (yes/no)
- **number vmail messages**: Number of voice mail messages

### Usage Statistics
- **total day minutes / calls / charge**: Daytime usage metrics
- **total eve minutes / calls / charge**: Evening usage metrics
- **total night minutes / calls / charge**: Nighttime usage metrics
- **total intl minutes / calls / charge**: International usage metrics

### Customer Service
- **customer service calls**: Number of calls made to customer service
- **churn**: Target variable (True/False), indicating whether the customer churned

## Business and Data Understanding

### Stakeholder Audience
The primary stakeholders for this project are customer retention and marketing teams at a telecommunications company, as well as customer service managers and senior leadership.

### Business Problem
Customer churn leads to lost revenue and increased costs associated with acquiring new customers. By identifying customers who are likely to churn before they leave, the business can prioritize outreach, improve customer service experiences, and design targeted retention offers.

### Why This Dataset Is Appropriate
The dataset includes customer demographics, service plans, call usage behavior, and customer service interaction data. These variables are directly relevant to churn behavior, making the dataset well-suited for a supervised classification task focused on churn prediction.

## Project Structure

```
OOP/Project/
├── Data/
│   └── bigml_59c28831336c6604c800002a.csv    # Customer churn dataset
└── notebooks/
    └── *.ipynb                               # Jupyter notebooks for analysis
```

## Getting Started

### Prerequisites
- Python 3.7+
- Required packages:
  - pandas
  - scikit-learn
  - numpy
  - matplotlib
  - seaborn
  - jupyter

### Installation

```bash
pip install pandas scikit-learn numpy matplotlib seaborn jupyter
```

## Usage

All data exploration, preprocessing, modeling, and evaluation are conducted in Jupyter notebooks located in the `notebooks/` directory. The notebooks document the full data science workflow from business understanding through final model evaluation.

## Modeling

An iterative modeling approach was used to address the churn classification problem:

- A simple, interpretable logistic regression model was used as a baseline.
- A tuned version of the baseline model improved performance while maintaining interpretability.
- A decision tree model was explored as a non-parametric alternative to capture potential nonlinear relationships.

Interpretability was prioritized throughout the modeling process to ensure that results could be clearly communicated to non-technical stakeholders and used to inform business decisions.

## Evaluation

Model performance was evaluated using classification metrics appropriate for churn prediction, with particular attention to metrics that reflect business impact (such as recall and ROC-AUC).

The final selected model was evaluated on a held-out test dataset to estimate performance on unseen customers and to prevent data leakage. Results were interpreted in terms of false positives and false negatives, emphasizing the risk of failing to identify customers who are likely to churn.

## Key Objectives

- Analyze customer behavior and churn patterns
- Build interpretable predictive models to identify at-risk customers
- Understand factors influencing customer churn
- Support data-driven customer retention strategies

## Conclusion

This project demonstrates how interpretable machine learning models can be used to proactively address customer churn in a telecommunications context. By identifying customers at high risk of leaving and highlighting the factors associated with churn, the analysis provides actionable insights that stakeholders can use to improve customer retention efforts.

Future work could include incorporating additional customer data, exploring ensemble models for comparison, or integrating the model into a live retention workflow.

## Contributing

This is an educational object-oriented programming (OOP) and machine learning project. Contributions and extensions are welcome for learning purposes.

## License

This project uses publicly available telecom data for educational purposes only.
