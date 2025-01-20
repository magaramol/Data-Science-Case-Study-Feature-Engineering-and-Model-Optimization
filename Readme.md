# NITS Data Science Case Study

## Overview

This project is a case study for the NITS Data Science position. The goal of the project is to build a model to predict a target variable based on four features. The dataset is provided by NITS Solutions and is not publicly available.

## Data Exploration and Preprocessing

- The dataset was explored using descriptive statistics, histograms, and scatter plots.
- Missing values were removed, retaining 99.74% of the original data.
- Outliers were identified using box plots and addressed using the Z-score method with a threshold of 2.
- The target variable was found to have a balanced distribution across its classes.
- Feature distributions were analyzed using KDE plots, revealing that most features follow a normal distribution except for 'feature4' and the target variable.
- Correlation between features and the target was assessed using a heatmap, indicating very low correlation.
- Scatter plots were used to visualize the relationship between features and the target, confirming the non-linear separability of the data.

## Baseline Model Building

Several baseline models were built to establish a performance benchmark, including:

- Random Forest (RF)
- Decision Tree (DT)
- XGBoost (Boosting)
- Naive Bayes (NB)
- Support Vector Machine (SVM)

The models were evaluated using accuracy, precision, recall, and F1-score. The accuracy of all models was close to random guessing, suggesting the need for further feature engineering.

## Feature Engineering

Various feature engineering techniques were applied to improve model performance:

- Polynomial Features
- Log Transformations
- Trigonometric Transformations
- Mutual Information Interaction
- Squared Features

## Model Evaluation and Selection

- The models were retrained using the engineered features and evaluated using the same metrics as before.
- Log Transformations consistently showed the best performance across all tree-based models, particularly with XGBoost achieving the highest accuracy.
- Despite improvements, the overall performance remained relatively low due to the inherent limitations of the dataset, including the lack of correlation with the target and multicollinearity.

## Conclusion

- Log transformation with XGBoost was identified as the most promising approach, though further exploration may be needed.
- The dataset's non-linearly separable nature and high multicollinearity pose challenges for achieving high accuracy.
- Advanced feature engineering techniques, feature selection, and exploring external data sources could potentially improve performance.

## Recommendations for Future Work

- Explore feature selection methods to identify the most relevant features.
- Consider more complex models or ensemble techniques to capture non-linear relationships.
- Investigate the possibility of incorporating external data sources to enrich the dataset.
- Perform hyperparameter tuning to optimize model performance.
