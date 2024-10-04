# Google Advanced Data Analytics Projects

First off I'd like to thank Google for putting together such a rigorous and engaging certificate program. The Google Advanced Data Analytics course offered an exceptional level of technical depth and expertise. It gave me an opportunity to refine my Python, EDA, statistics and advanced machine learning skills. The program’s focus on real-world scenarios, like classifying TikTok videos as claims or opinions, allowed me to work on interesting problems and apply new analytical skills. 

This repository contains the Jupyter notebooks from the capstones for the four most interesting classes, and covers a wide range of data analysis topics. One of the other cool things about the Google's Advanced Data Analytics certificate is that it allows you apply all aspects of the PACE framework to dataset. So the more you invest in each part the more interesting the results in the subsequent sections:

- **Exploratory Data Analysis (EDA)**: Insights into TikTok video data using Python and pandas.
- **Statistics**: Application of descriptive and inferential statistics, probability distributions and hypothesis testing in Python.
- **Regression**: Predicting TikTok video characteristics using linear regression.
- **Machine Learning**: Modeling video engagement features with classification models.

Before we get into the concepts and tools applied, let's get into the fun stuff...

## Easter Eggs Found 🥚  
It seems that Google might have embedded some subtle challenges in each capstone project, which can be uncovered with careful analysis: **Spoiler alert**:
- **Lab 3-EDA**: During exploratory data analysis, you’ll notice that there are no claim videos with fewer than ~1K views in a sample of over 9K claim videos. This anomaly suggests potential filtering or bias in the data collection process, as it’s statistically improbable to observe such a strict cutoff without external influence.
- **Lab 4-Statistics**: The team proposes a two-sample hypothesis test to assess whether there is a statistically significant difference in the number of views between TikTok videos posted by verified and non-verified creators. However, if you don’t examine the assumptions of the test, you’ll miss that two key conditions—normal distribution and random sampling—are violated. This oversight can lead to invalid conclusions if not addressed appropriately with alternative methods or adjustments.
- **Lab 5-Regression**: The dataset provided has a 94%–6% class imbalance in the target variable. If you follow the outlined process exactly, you might upsample the minority class before splitting the data, which introduces data leakage. This leakage occurs because the synthetic data created during upsampling contains information from the entire dataset. A quick check reveals 1,131 exact matches between the training and test sets. To avoid this issue, techniques like SMOTE should only be applied after the data split to ensure a clean separation between training and testing sets.
- **Lab 6-Modeling**: A baseline Random Forest model yields an accuracy of over 95% in predicting whether videos are claims or opinions. While this may seem like excellent performance, an experienced analyst will recognize this as a sign of potential overfitting. Upon further inspection, the underlying issue is that the dataset is too easy to classify, pointing to a data quality problem disguised as a model performance problem.

## Concepts & Tools
### 1. [TikTok_ProjectLab_3_EDA.ipynb](./TikTok_ProjectLab_3_EDA.ipynb)
- **Concepts**:
  - Exploratory Data Analysis (EDA)
  - Feature Engineering
  - Data Cleaning
  - Correlation Analysis
  - Data Visualization
- **Tools**:
  - Pandas 
  - Seaborn 
  - Matplotlib 
  

### 2. [TikTok_ProjectLab_4_Statistics.ipynb](./TikTok_ProjectLab_4_Statistics.ipynb)
- **Concepts**:
  - Cluster Sampling
  - Hypothesis Testing
  - Descriptive Statistics
  - Confidence Intervals
  - p-value Interpretation
  - Statistical Inference

- **Tools**:
  - Two-sample z-test for proportions
  - Mann-Whitney U test for distribution difference
  - Statsmodels 
  - Scipy.stats 
  - Matplotlib 
  - Pandas


### 3. [TikTok_ProjectLab_5_Regression.ipynb](./TikTok_ProjectLab_5_Regression.ipynb)
- **Concepts**:
  - Linear Regression
  - Multiple Regression
  - Model Evaluation (R-squared, Adjusted R-squared)
  - Feature Transformation (logarithmic, polynomial)
  - Multicollinearity
- **Tools**:
  - SMOTE sampling 
  - One Hot Encoding
  - Statsmodels 
  - VIF (Variance Inflation Factor)
  - Correlation Matrix (SNS Heatmap)


### 4. [TikTok_ProjectLab_6_Modeling.ipynb](./TikTok_ProjectLab_6_Modeling.ipynb)
- **Concepts**:
  - Classification
  - Hyperparameter Tuning
  - Cross-validation
  - Confusion Matrix
  - ROC Curve and AUC
- **Tools**:
  - XGBoost 
  - Random Forest Classifier, 
  - Grid Search, 
  - Randomized Search,
  - Optuna Search
  - Confusion Matrix
  - Custom metric
