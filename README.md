Multiple Linear Regression - Multi-Channel Marketing
Analysis
Project Overview
This project analyses a marketing dataset (TV, Radio, Social Media, Influencer) to build a
Multiple Linear Regression model predicting Sales. We check for multicollinearity using VIF,
select significant predictors using Adjusted R-squared and p-values, validate OLS
assumptions with diagnostic plots, and deliver a prioritised budget recommendation.
Dataset
File: marketing_and_sales_data.csv
Rows: 572 | No missing values | No duplicates
Columns:
TV – Categorical: Low / Medium / High (ordinal encoded 1/2/3)
Radio – Continuous: radio advertising spend ($000s)
Social Media – Continuous: social media advertising spend ($000s)
Influencer – Categorical: Macro / Mega / Micro / Nano (one-hot encoded)
Sales – Continuous: sales revenue ($000s) [TARGET]
Environment Setup
pip install pandas numpy matplotlib seaborn scipy
Run the notebook:
jupyter notebook multiple_regression_analysis.ipynb
Key Results
Model Predictors Adj R2 RMSE
Full (TV+Radio+SocMed+Influencer) 6 0.9031 27.98
Reduced (TV+Radio+SocMed) 3 0.9034 27.93
Final (TV+Radio) 2 0.9036 27.91
Final Model Equation: Sales = 77.32 x TV_encoded + 2.96 x Radio - 12.39
Multicollinearity: All VIF values < 4 (well below threshold of 10) – no issue.
Social Media (p=0.815) and all Influencer types (p > 0.35) were not significant and excluded
from the final model.
Assumption Tests
Assumption Test Result
Linearity Corr(predictors, residuals) ~0.000 – PASS
Normality Q-Q plot + Shapiro-Wilk Approx. normal – PASS
Homoscedasticity Corr(fitted, residuals) r=-0.025 – PASS
Independence Durbin-Watson DW=1.876 – PASS
Recommendation
1. Maximise TV spend (allocate 60-65% of budget) – highest impact channel
2. Invest in Radio as secondary channel (25-30%) – consistent $2,960 per $1K
3. Deprioritise Social Media – not a significant predictor in this dataset
4. Influencer tier does not significantly affect Sales
