Multiple_Regression_Analysis –A Multi-Channel Marketing Analysis

Project Overview

This project analyzes a multi-channel marketing dataset using Python to construct a statistically robust Multiple Linear Regression model. The main focus is to isolate how TV, Radio, and Social Media budgets collectively influence unit Sales, detect any underlying multicollinearity issues, and interpret the model parameters to provide an optimized corporate marketing strategy.

Core Project Goals

Exploratory Data Analysis (EDA): Visualize multi-channel continuous trends using scatter matrices and joint plot distributions.
Multicollinearity Diagnosis: Evaluate predictor-to-predictor overlapping relationships using Pearson correlation and Variance Inflation Factors (VIF).
Multivariate OLS Modeling: Fit a multiple regression model to evaluate the simultaneous impact of variables on Sales.
Assumption Validation: Confirm model reliability via residual testing (Linearity, Normality, and Homoscedasticity).
Strategic Reallocation: Deliver clear budget priorities to stakeholders based on variable coefficients and statistical significance boundaries.
Local Installation & Environment Setup

To set up your local environment and reproduce this analysis, ensure you have Python installed, clone this repository, and install the required libraries:

# Clone the repository to your local system
git clone https://github.com

# Navigate into the project folder
cd multiple_regression_analysis

# Install dependencies using pip
pip install pandas numpy matplotlib seaborn statsmodels scipy scikit-learn
Key Analytical Findings & Model Diagnostics

Our multivariate Ordinary Least Squares (OLS) regression model evaluated 572 active campaigns and generated the following high-value metrics:

Adjusted R-squared (
0.903
): Our combined media ecosystem successfully explains 90.3% of all historical sales variations, confirming strong forecasting stability.
TV Tier Parameter (
β
T
V
=
77.3227
): Holding Radio and Social Media budgets constant, advancing a market up by one investment tier (e.g., Medium to High) results in a massive average lift of 77.32 units in Sales (
p
<
0.001
).
Radio Parameter (
β
R
a
d
i
o
=
2.9792
): Holding TV and Social Media investment constant, each additional dollar committed to Radio yields a highly significant linear return of 2.98 units in Sales (
p
<
0.001
).
The Social Media Redundancy Trap (
p
=
0.815
): While Social Media initially showed moderate correlation, its high p-value proves it adds zero new value when Radio is present. It is statistically insignificant and redundant dead weight.
Model Stability (Durbin-Watson = 
1.874
): Sits closely to the target baseline of 2.0, proving independence of data points and zero background time-sequencing bias.
Actionable Business Recommendation

Defund Social Media Immediately: Pull 100% of current Social Media capital. Because it overlaps with Radio (
r
=
0.63
), it fails to target new audiences and contributes nothing to independent revenue growth.
Scale TV Packages: TV yields our single largest margin jump. Prioritize scaling markets into higher TV investment tiers.
Maintain Radio Momentum: Maintain consistent capital injections into Radio channels as a secure, verified revenue driver.
Operational Forecasting: Utilize the validated multivariate model equation to project upcoming quarterly revenue lines:
