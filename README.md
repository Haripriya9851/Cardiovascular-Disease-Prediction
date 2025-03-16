# Cardiovascular-Disease-Risk-Prediction
ML Risk Model for Cardiovascular Disease Prediction

Overall, our analysis confirms that age, smoking, and diabetes have a statistically significant impact on cardiovascular disease, while BMI alone is not a primary predictor. 

# Problem Statement & Objective of the Analysis:
Heart disease remains the leading cause of death in the United States, with approximately 697,000 fatalities in 2021 (CDC, 2023). This study analyzes the Personal Key Indicators of Heart Disease dataset from Kaggle, derived from CDC surveys, to identify key risk factors across U.S. states. Given the influence of both medical and behavioral factors, the findings aim to inform healthcare professionals and public health strategies for early intervention and prevention.
# Methodology:
The analysis was done in several steps leveraging R Programming:
**Exploratory Data Analysis (EDA):** This phase involved handling data integration potential data issues, along with plotting visualization graphs to derive insights and business questions for the relationships between the demographic,behavioral factors and the target variable.
**Hypothesis Testing:**
Our analysis explored four key hypotheses related to cardiovascular disease: the impact of age, BMI, smoking, and diabetes on heart disease occurrence. 
- The results strongly support the hypothesis that older individuals are more likely to experience cardiovascular events, as the median age of those with heart disease is significantly higher.
- Similarly, smoking or alcohol consumption exhibits a clear trend, with a greater proportion of smoking or alcohol consumers experiencing cardiovascular disease, reinforcing the well-established link between smoking and heart-related health risks.
- Diabetes also emerges as a critical factor, as individuals with diabetes, particularly those with a confirmed diagnosis, show a noticeably higher prevalence of cardiovascular events compared to non-diabetics. These findings validate the role of diabetes in increasing heart disease risk.
- BMI was 
**Logistic Regression:** A logistic regression model was fit to predict the , considering age,BMI, as predictors.
**Decision-Tree modeling:**  To understand non-linear patterns tree based Randomforest and XGBoost model were fit.
**Feature Selection:** The PCA was employed to assess feature importance and select the most relevant predictors of CVD risk.
