# Company Bankruptcy Classification
## By Daniel Chang and Joey Hernandez

## Introduction

Bankruptcy is a legal process that occurs when a company or individual cannot meet their due debts. This phenomenon has significant economic implications on both micro and macro scales. This project aims to construct a predictive model to determine the likelihood of a company going bankrupt within a specified forecasting period after its financial evaluation. 

## Objective and Scope

The primary objective is to guide investors in their decision-making processes, aid regulators in overseeing corporate health, and enable businesses to introspect and fortify their financial strategies.

To achieve this, we will employ Random Forest and XGBoost algorithms, both of which are adept at handling complex datasets and can provide insights into the factors influencing bankruptcy risk among companies.

## Addressing Class Imbalance

Recognizing that datasets often have an unequal distribution of classes, we will employ class imbalancing techniques such as oversampling, undersampling, and synthetic data generation using SMOTE (Synthetic Minority Over-sampling Technique) to ensure that our model is not biased towards the majority class.

## Optimization using Random CV Search

To fine-tune the parameters of our chosen algorithms, we will leverage Randomized Cross-Validation Search. This method provides a more efficient approach than exhaustive search, sampling a fixed number of parameter settings from the specified distributions. This ensures an optimal mix of parameters, enhancing the model's predictive capabilities.

## Data Inspection

A rigorous inspection of the dataset was performed, involving steps such as Descriptive Statistics, Data Types Assessment, Missing Values Identification, Unique Values Examination, Distribution Analysis, Correlation Analysis, Class Distribution Check, Data Consistency Check, and Temporal Consistency.

## Target Variable Inspection

The distribution of our target variable was closely inspected, distinguishing between "Not-Bankrupt" and "Bankrupt" categories. The presence of class imbalance was noted, with "Bankrupt" instances forming a minority in each year.

## Missing Data

To address challenges associated with missing data, we adopted a two-pronged strategy. For values that showed high correlations in their missing patterns, we opted for median imputation. On the other hand, features like 'Attr21' and 'Attr22' with more than half of their values missing were removed from our dataset.

## Modeling

### Random Forest

The Random Forest algorithm was employed, which is a versatile ensemble learning method that aggregates multiple decision trees to improve prediction accuracy and control over-fitting. Key steps included Class Weight Adjustment, Random Search for Parameter Tuning, and Train-Test Split.

### XGBoost

The XGBoost framework was used, known for its speed and accuracy. Key steps involved Data Preparation, Conversion to DMatrix, Cross Validation with Early Stopping, Visualization, Hyperparameter Tuning, and Model Evaluation.

## Results

Results for both Random Forest and XGBoost models across all years indicated a consistently high precision for the "Not Bankrupt" category and high recall for the "Bankrupt" category. The overall accuracy ranged from 0.81 to 0.88 across the five years.

## Ensemble Report AUC Performance Comparison

The performance of the models developed under the SMU MSDS framework was evaluated against another benchmark model presented in a research paper. The MSDS model exhibited consistent and competitive AUC scores, often showcasing similar or marginally higher values compared to the benchmark model.

## Conclusion

The models developed under the SMU MSDS framework demonstrated high efficacy in predicting company bankruptcy over the observed period. They consistently outperformed or matched the established benchmark, underscoring the potential of the modeling approach adopted.

## Recommendations

1. Adopting Ensemble Techniques: Continuous adoption of ensemble techniques, such as Random Forest and XGBoost, is recommended due to their ability to aggregate multiple individual predictions and significantly enhance prediction accuracy.

2. Addressing Imbalances with Caution: Class imbalances should be addressed using techniques like SMOTE. However, care must be taken to ensure synthetic data generation does not introduce noise or bias into the predictions.

3. Optimization is Key: Hyperparameter optimization through methods like Randomized CV Search is crucial. Other optimization techniques should be explored for enhanced results.

4. Precision vs. Recall: Decision-makers should weigh the costs associated with false positives versus false negatives and consider adjusting the optimal threshold based on specific use-case scenarios.

5. Addressing Missing Financial Data: Imputation techniques for missing financial data should be continued, ensuring data integrity.