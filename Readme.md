
# Data Science Case Study: Predicting Target Variable with Feature Engineering  

## Overview  

This project focuses on building a predictive model for a given dataset using four features. The goal is to develop a robust model that accurately predicts the target variable while addressing challenges such as feature correlation, non-linearity, and data preprocessing.  

## Data Exploration and Preprocessing  

- The dataset was analyzed using descriptive statistics, histograms, and scatter plots.  
- Missing values were removed, retaining 99.74% of the original data.  
- Outliers were identified and addressed using the Z-score method with a threshold of 2.  
- The target variable exhibited a balanced distribution across classes.  
- Kernel Density Estimation (KDE) plots revealed that most features followed a normal distribution, except for 'feature4' and the target variable.  
- Correlation analysis using a heatmap indicated low correlation between features and the target.  
- Scatter plots confirmed the dataset’s non-linear separability.  

## Baseline Model Building  

Several baseline models were implemented to establish a performance benchmark:  

- Random Forest (RF)  
- Decision Tree (DT)  
- XGBoost (Boosting)  
- Naive Bayes (NB)  
- Support Vector Machine (SVM)  

The models were evaluated using accuracy, precision, recall, and F1-score. The results suggested performance close to random guessing, highlighting the need for further feature engineering.  

## Feature Engineering  

To enhance model performance, various transformations were applied:  

- Polynomial Features  
- Log Transformations  
- Trigonometric Transformations  
- Mutual Information Interaction  
- Squared Features  

## Model Evaluation and Selection  

- Models were retrained using the engineered features and evaluated using the same metrics.  
- Log Transformations yielded the best performance across all tree-based models, with XGBoost achieving the highest accuracy.  
- Despite improvements, performance remained limited due to dataset constraints such as low feature-target correlation and multicollinearity.  

## Conclusion  

- Log transformation combined with XGBoost showed the most promising results, though additional refinements may be necessary.  
- The dataset’s challenges, including non-linearity and multicollinearity, made achieving high accuracy difficult.  
- Advanced feature engineering, feature selection, and additional data sources could improve future performance.  

## Recommendations for Future Work  

- Implement feature selection methods to retain only the most relevant variables.  
- Explore complex models or ensemble techniques to better capture non-linear relationships.  
- Investigate external data sources to enhance the dataset.  
- Perform hyperparameter tuning for further model optimization.  
