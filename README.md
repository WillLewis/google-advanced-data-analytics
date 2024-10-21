# Google Advanced Data Analytics Projects

First off I'd like to thank Google for putting together such a rigorous and engaging curriculum. Having spent my fair share of time in tough classes I'd say the Google Advanced Data Analytics course offered an high level of technical depth and the sort of insights you'd expect from Googlers. Its not for everyone - but its just flexible enough that you can spend anywhere from one week to one month per class. I spent closer to the former on classes 1-2, somewhere in between on 3 and 4 and the later on classes 5-6.  It gave me an opportunity to refine my Python, EDA, statistics and advanced machine learning skills. The program’s focus on real-world scenarios, like classifying TikTok videos as claims or opinions, presented interesting problems and an opportunity to learn and apply new analytical skills. 

This repository contains the Jupyter notebooks from the capstones for the four most interesting classes, and covers a wide range of advanced data analysis topics. One of the cool things about the Google's Advanced Data Analytics certificate is that it allows you apply all aspects of the PACE framework across a particular dataset for the capstones. So your work builds on itself and the more you invest, the more interesting the results in the subsequent sections, until - as many things in data science - you reach the point of diminishing returns, which I consider the point I can relax:

- **Exploratory Data Analysis (EDA)**: Insights into TikTok video data using Python numpy, pandas, seaborn, matplotlib.pyplot to analyze distributions, conduct feature transformation and feature transformation.
- **Statistics**: Application of descriptive and inferential statistics, probability distributions and hypothesis testing in Python.
- **Regression**: Predicting TikTok video characteristics using linear regression.
- **Machine Learning**: Modeling video engagement features with RandomForest, XGBBoost and other models.
- **Capstone Project**:  Analyze the data of a recent survey along with employee data to design a model that predicts whether an employee will leave the company based on their  department, number of projects, average monthly hours, and any other data points and explain what is driving turnover. This capstone project includes a bit of everything from EDA to modeling to synthesizing the analysis into actionable insight.


Before we get into the details of the concepts and tools applied, let's touch on the fun stuff...

## Easter Eggs Found 🥚  
It seems that Google might have embedded some subtle challenges in each capstone project, which can be uncovered with careful analysis: **Spoiler alert**:
- **Lab 3-EDA**: During exploratory data analysis, you’ll notice that there are no claim videos with fewer than ~1K views in a sample of over 9K claim videos. This anomaly suggests potential filtering or bias in the data collection process, as it’s statistically improbable to observe such a strict cutoff without external influence.
- **Lab 4-Statistics**: The team proposes a two-sample hypothesis test to assess whether there is a statistically significant difference in the number of views between TikTok videos posted by verified and non-verified creators. However, if you don’t examine the assumptions of the test, you’ll miss that two key conditions—normal distribution and random sampling—are violated. This oversight can lead to invalid conclusions if not addressed appropriately with alternative methods or adjustments.
- **Lab 5-Regression**: The dataset provided has a 94%–6% class imbalance in the target variable. So you have If you follow the outlined process exactly, you might upsample the minority class before splitting the data, which introduces data leakage. This leakage occurs because the synthetic data created during upsampling contains information from the entire dataset. A quick check reveals 1,131 exact matches between the training and test sets. To avoid this issue, techniques like SMOTE should only be applied after the data split to ensure a clean separation between training and testing sets.
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
  - ROC AUC
- **Tools**:
  - XGBoost 
  - Random Forest Classifier, 
  - Grid Search, 
  - Randomized Search,
  - Optuna Search
  - Confusion Matrix
  - Custom metric


  ### 5. [CapstoneProject_SalifortMotors_TurnoverAnalysis.ipynb](./CapstoneProject_SalifortMotors_TurnoverAnalysis.ipynb)
- **Concepts**:
  - Cox Proportional Hazard 
  - Classification
  - Hyperparameter Tuning
  - Cross-validation
  - Confusion Matrix
  - ROC AUC
- **Tools**:
  - XGBoost 
  - Random Forest Classifier 
  - Optuna Search
  - Confusion Matrix
  - Custom metric
