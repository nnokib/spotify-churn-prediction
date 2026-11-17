# spotify-churn-prediction
## Spotify Churn Analysis and Prediction
1. Objective
To identify behavioural and demographic indicators of customer attrition within an 8,000-user Spotify dataset and build a machine learning model to predict churn, translating technical findings into actionable retention strategies.

2. Data Source

Dataset: Spotify User Behaviour Dataset (8,000 records, 12 features).

Features: Demographics (gender, age, country), Subscription Type (free, premium, student, family), and Engagement Metrics (listening time, songs played per day, skip rate, device type, ads listened, offline listening).

3. Tools Used

Language: Python (Jupyter Notebook)

Data Manipulation: pandas, NumPy

Visualisation: seaborn, matplotlib

Statistical Analysis: SciPy (Chi-Square, Welch's T-Test)

Machine Learning: scikit-learn (Random Forest, Logistic Regression, KNN, Decision Tree)

4. Methodology

Exploratory Data Analysis (EDA) & Preprocessing: Conducted univariate and multivariate analysis to identify distributions and class balance (25.9% churn rate). Handled outliers in ad exposure using IQR trimming and capping.

Statistical Significance Testing: Applied Chi-Square tests for categorical variables and Independent Samples T-Tests for numerical variables. Correlation heatmaps revealed that no single feature had a strong linear relationship with churn (the highest correlation was skip_rate at just 0.016).

Predictive Modelling: Built and benchmarked multiple classification models using an 80/20 train-test split. Extracted feature importance from the best-performing ensemble model.

5. Key Insights & Model Performance

Non-Linearity is Key: Traditional linear models failed to capture churn drivers. The Random Forest algorithm delivered superior performance, achieving a peak predictive accuracy of 75.1% and a precision score of 0.60 by effectively capturing complex feature interactions.

Engagement > Demographics: Feature importance analysis proved that listening time, songs played per day, skip rate, and age are the dominant predictors of retention. Categorical variables (gender, country, subscription type) showed no statistically significant impact on churn.

The Listening Time Threshold: Temporal analysis showed a distinct gap where non-churned users consistently maintained higher average listening times, making a drop in listening time the strongest early warning signal for attrition.

6. Actionable Business Recommendations

Algorithmic Optimisation: Deploy smarter recommendation algorithms to directly target and reduce user skip_rate, keeping users engaged for longer sessions.

Targeted Re-engagement: Initiate proactive marketing and re-engagement campaigns for users showing early signs of dropping below baseline listening times.

Pricing Strategy: Address cost sensitivity in the 15-30 age demographic (which constitutes ~1/3 of the user base) by evaluating discounted tiers to improve retention.
