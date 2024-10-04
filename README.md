# Google Advanced Data Analytics Projects

First off I'd like to thank Google for putting together such a rigorous and engaging certificate program. The Google Advanced Data Analytics course offered an exceptional level of technical depth and expertise. It gave me an opportunity to refine my Python, EDA, statistics and advanced machine learning skills. The program’s focus on real-world scenarios, like classifying TikTok videos as claims or opinions, allowed me to work on interesting problems and apply new analytical skills. 

This repository contains the Jupyter notebooks from the capstones for the four most interesting classes, and covers a wide range of data analysis topics. One of the other cool things about the Google's Advanced Data Analytics certificate is that it allows you apply all aspects of the PACE framework to dataset. So the more you invest in each part the more interesting the results in the subsequent sections:

- **Exploratory Data Analysis (EDA)**: Insights into TikTok video data using Python and pandas.
- **Statistics**: Application of descriptive and inferential statistics, probability distributions and hypothesis testing in Python.
- **Regression**: Predicting TikTok video characteristics using linear regression.
- **Machine Learning**: Modeling video engagement features with classification models.

Before we get into the concepts and tools applied, let's get into the fun stuff...

## Easter Eggs Found 🥚
It seems that Google might have had some fun here planting easter eggs in each capstone project, which can be discovered with the right amount of analytical rigour: **Spoiler alert**:
- **Lab 3-EDA**: With the appropriate EDA you'll notice that there were no claim videos with less than ~1K views in a sample of >9K claim videos. This is highly unlikely.
- **Lab 4-Statistics**: Your team proposes a two-sample hypothesis test to determine whether there is a statistically significant difference in the number of views between TikTok videos posted by creators with different verification status. If EDA isn't conducted in the prior class you won't know that a two assumptions for a two-sample hypothesis are violated -- normal distribution and random sampling. So if you simply follow the proposed approach and don't take additional steps you're doomed from the start.  
- **Lab 5-Regression**: You are provided with a dataset that has 94% - 6% class imbalance in the target variable. If you follow the process outlined to the letter you end up upsampling before splitting the data. And if you upsample before you split you end up with data leakage as you've created synthetic data that is influenced by the entire dataset. So the model sees patterns that reflect information from both the training and test set. A quick test reveals 1,131 exact matches across test and training sets unless you use a technique like SMOTE for upsampling. 
- **Lab 6-Modeling**: A baseline Random Forest Model reveals a baseline performance >95% in predicting whether videos are claims or opinions. And while the problem is framed as if increasing performance is the objective, an experienced will think that >95% is too high and the problem is model overfitting. But with appropriate modeling you realize the problem is the data is in fact, too easy to classify. So its a data problem wrapped in a overfitting problem wrapped in a performance problem. Well done Google, well done.


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
