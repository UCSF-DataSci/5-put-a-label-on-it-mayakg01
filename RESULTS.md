# Assignment 5: Health Data Classification Results

This file contains your manual interpretations and analysis of the model results from the different parts of the assignment.

## Part 1: Logistic Regression on Imbalanced Data

### Interpretation of Results

In this section, provide your interpretation of the Logistic Regression model's performance on the imbalanced dataset. Consider:

- Which metric performed best and why?
- Which metric performed worst and why?
- How much did the class imbalance affect the results?
- What does the confusion matrix tell you about the model's predictions?

**Analysis:**
- The accuracy metric performed best, while the recall metric performed worst. The confusion matrix tells us how the errors were split between false negatives and false positives. Recall was likely higher because of the class imbalance; the model was more frequently predicting the majority class with a greater number of false negatives (not as correctly predicting the minority class). The minority class was a disease outcome of no disease, while the majority class was a disease outcome of disease.

## Part 2: Tree-Based Models with Time Series Features

### Comparison of Random Forest and XGBoost

In this section, compare the performance of the Random Forest and XGBoost models:

- Which model performed better according to AUC score?
- Why might one model outperform the other on this dataset?
- How did the addition of time-series features (rolling mean and standard deviation) affect model performance?

**Analysis:**
- The XGBoost tree performed better (AUC score of 0.9953 vs. AUC of 0.9724).
- The time series features boosted model performance by keeping track of how the mean and sd changed over time.

## Part 3: Logistic Regression with Balanced Data

### Improvement Analysis

In this section, analyze the improvements gained by addressing class imbalance:

- Which metrics showed the most significant improvement?
- Which metrics showed the least improvement?
- Why might some metrics improve more than others?
- What does this tell you about the importance of addressing class imbalance?

**Analysis**:
- Recall showed the most significant improvement, improving by 183.72%
- Precision got worse by the greatest amount
- Accuracy and AUC were not greatly affected by addressing class imbalance
- Results show that class imbalance is largely important for addressing low recall

## Overall Conclusions

Summarize your key findings from all three parts of the assignment:

- What were the most important factors affecting model performance?
- Which techniques provided the most significant improvements?
- What would you recommend for future modeling of this dataset?

**Conclusions**
- Extracting rolling features and calculating rolling statistics was beneficial for model performance
- Random Forest & XGboost both had strong performance
- Addressing class imbalance is important when you want to prioritize improving a low recall statistic