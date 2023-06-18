# Facebook Dataset Analysis

This repository contains code and analysis for exploring a Facebook dataset. The dataset comprises several features like gender, age, tenure, likes received, etc. It can be used for advanced analytics and improved user experience. The main objective of this analysis is to predict the value of the "gender" feature, making it a classification problem.

## Repository Contents

- `facebook.csv`: The dataset file in CSV format. (Removed for Further modification)
- `analysis.ipynb`: Jupyter Notebook containing the code and analysis.
- `README.md`: This file providing an overview of the repository.

## How to Run

1. Clone this repository.
2. Install the necessary dependencies: pandas, numpy, matplotlib, and seaborn.
3. Open the `analysis.ipynb` notebook in Jupyter Notebook or any compatible environment.
4. Run the code cells in the notebook to perform the analysis and generate visualizations.

## Initial Data Exploration

The initial data exploration includes plotting histograms, box plots, correlation matrices, subplots of numerical features, and count plots of categorical variables.

After filling the missing values using the backfill method, the following steps were performed:

- Histograms and box plots were used to visualize the distributions and identify outliers.
- Correlation matrix and bar plots of mean values for each feature were generated to understand the relationship between features and the target variable.
- The features with low correlation to the target variable ('gender') were dropped.
- Robust scaling was applied to handle outliers and scale the remaining features.

## Findings

Based on the analysis, the following findings were observed:

1. The features 'likes', 'mobile_likes', 'www_likes', 'friend_count', 'tenure', 'age', 'likes_received', 'www_likes_received', and 'mobile_likes_received' show a positive correlation with the target variable ('gender').
2. The feature 'dob_year' shows a negative correlation with 'gender'.
3. The remaining features do not have a significant relationship or correlation with 'gender' and can be dropped.

## Hypotheses

The following hypotheses were formulated based on the dataset:

1. The mean number of likes received by the two genders is different.
2. Likes increase with the passage of tenure (likes_received is directly proportional to tenure).
3. Females receive more likes than males for the same level of friendship initiation.

To test these hypotheses, bar plots and point plots were created to visualize the relationships between variables.

## Suggestions for Further Analysis

Based on the findings and observations from the analysis, the following suggestions are made for further analysis:

1. Consider applying power transformations to achieve a more Gaussian-like distribution of the data.
2. Explore outlier removal algorithms or density-based clustering algorithms to clean the data and improve the analysis.

## Conclusion

The Facebook dataset exhibits average data quality with limited highly correlated features related to the target variable 'gender'. Outliers were identified and addressed using robust scaling. The analysis reveals a slight inclination towards males based on the average values of the features. If additional data related to user behavior, interests, or demographics is available, it could enhance the analysis and provide deeper insights into user preferences.

For more details, refer to the `analysis.ipynb` notebook in this repository.
