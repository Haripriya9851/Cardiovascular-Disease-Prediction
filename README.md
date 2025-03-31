# Cardiovascular-Disease-Risk-Prediction
Group Project on ML Risk Model for Cardiovascular Disease Prediction

Overall, our analysis confirms that age, medical history like COPD and diabetes, lifesyle factors like sleep hours, smoking, alcohol consumption  have a statistically significant impact on incidence of cardiovascular disease, while BMI alone is not a primary predictor. 

# Problem Statement & Objective of the Analysis:
Heart disease remains the leading cause of death in the United States, with approximately 697,000 fatalities in 2021 (CDC, 2023). This study analyzes the Personal Key Indicators of Heart Disease dataset from Kaggle, derived from CDC surveys, to identify key risk factors across U.S. states. Given the influence of both medical and behavioral factors, the findings aim to inform healthcare professionals and public health strategies for early intervention and prevention.

# Methodology:
The analysis was done in several steps leveraging R Programming:

**Exploratory Data Analysis (EDA):** This phase involved handling data integration potential data inconsistencies, along with plotting visualization graphs to derive insights and business questions for the relationships between the demographic,behavioral factors and the target variable.

**Hypothesis Testing:**
Our analysis explored four key hypotheses related to cardiovascular disease: the impact of Age, BMI, smoking/alcohol consumption, and diabetes on heart disease occurrence. 
- The results strongly support the hypothesis that older individuals are more likely to experience cardiovascular events, as the median age of those with heart disease is significantly higher.
- Similarly, smoking or alcohol consumption exhibits a clear trend, with a greater proportion of smoking or alcohol consumers experiencing cardiovascular disease, reinforcing the well-established link between smoking and heart-related health risks.
- Diabetes also emerges as a critical factor, as individuals with diabetes, particularly those with a confirmed diagnosis, show a noticeably higher prevalence of cardiovascular events compared to non-diabetics. These findings validate the role of diabetes in increasing heart disease risk.
- BMI does not exhibit a strong correlation with cardiovascular disease. While individuals with higher BMI values are slightly more represented in the heart disease group, the overlap between those with and without heart disease suggests that BMI alone may not be a definitive risk factor.

**Logistic Regression:**

<img width="329" alt="image" src="https://github.com/user-attachments/assets/63bc35d5-1c3d-4539-ba39-f07847c6b875" />

The logistic regression model revealed several key predictors of cardiovascular risk, with p-values providing insight into their significance. Further, the bar chart, was plotted to identify significant predictors based on p-values. Chronic obstructive pulmonary disease (COPD) emerged as a highly significant factor, with a p-value approaching zero (p=0.00), indicating a strong and reliable association with cardiovascular events. Similarly, sex, age category, diabetes, arthritis, and depressive disorder all recorded p-values well below the conventional significance threshold  (p<0.05), confirming their critical roles as risk factors. Protective variables, such as engagement in physical activity (p=0.91) and adequate sleep (p=0.008), also showed statistically significant relationships, supporting their influence in lowering cardiovascular risk. In contrast, some variables, including BMI (p=0.057) and alcohol or smoking habits (p=0.056), presented higher p-values that exceeded the 0.05 threshold, suggesting that their relationships with cardiovascular events are weaker or possibly confounded by other factors. The consistently low p-values of key health conditions and demographic variables underline their importance in accurately assessing cardiovascular risk within the model.



**Decision-Tree modeling:**  
<img width="329" alt="image" src="https://github.com/user-attachments/assets/06b9108e-b7f2-4d84-87a3-98e5f1d4000a" />


To understand non-linear patterns tree based Randomforest and XGBoost model were fit.
The Random Forest model was trained using the undersampled preprocessed dataset and was particularly effective in capturing non-linear interactions between features. Feature importance analysis showed that BMI was the most influential predictor, followed by age category and sleep hours. Conditions like diabetes and arthritis also had substantial importance, consistent with known risk factors. Race/ethnicity had a more moderate impact, while COPD, which was the top predictor in the logistic regression model, showed relatively less importance here, suggesting that its influence may be more linear.


**Feature Selection:** The PCA was employed to assess feature importance and select the most relevant predictors of CVD risk.

Conclusion:
This study applied a comprehensive data mining approach to the Heart Risk dataset, incorporating data cleaning, exploratory analysis, hypothesis testing, and machine learning models to understand the complex relationships between demographic, behavioral, and clinical factors and
cardiovascular event risk.

![image](https://github.com/user-attachments/assets/b1dbdf89-3072-4cb2-84b3-c03e1e54fbb9)

Table 1 presents a summary of predictive performance across the three models. Although the PCA-based Random Forest model achieved the highest accuracy at 88.03%, it demonstrated poor recall (0.071) and an F1-score of only 0.1214. This imbalance indicates that the model struggled to correctly identify high-risk individuals, making it less reliable for healthcare applications where minimizing false negatives is crucial. In contrast, the Logistic Regression model, with a lower accuracy of 72.12%, achieved the best F1-score (0.73) and recall (0.76), demonstrating a better balance between identifying at-risk individuals and avoiding false positives. The Random Forest model had comparable but slightly weaker performance in both precision and recall. Given this evaluation, the under-sampled Logistic Regression model is preferred for its consistent and interpretable results, especially as its high recall minimizes false negatives, in the context of cardiovascular disease screening. 

Based on the Logistic Regression coefficients and Feature Importance from the Random Forest model, age, health conditions like diabetes, pulmonary disease and lifestyle factors like physical activity, BMI, sleep hours emerged as the strongest predictors of cardiovascular risk, aligning with EDA insights.

Based on these insights, the following recommendations are proposed for public health policymakers and data owners: Health department should implement targeted preventive programs by introducing early screening initiatives for older adults and individuals with pre-existing conditions like diabetes and COPD to detect cardiovascular risks early and enable timely interventions. Additionally, promoting on healthy lifestyles through public awareness campaigns, especially for high-risk elderly group in community centers,  emphasizing regular physical activity, balanced nutrition, and adequate sleep is crucial in reducing cardiovascular risk factors can support preventive efforts.  Ensuring accessibility to healthcare for high-risk individuals, particularly in underserved or rural areas, is essential by providing affordable screenings, medications, and lifestyle coaching to mitigate risks before they escalate into severe conditions. These strategies will help reduce disparities in cardiovascular health outcomes and enhance preventive care, ultimately contributing to a healthier population with a lower incidence of heart-related diseases. 
![image](https://github.com/user-attachments/assets/1894764c-66ec-4165-b6dc-65100a96fd9f)



Reference

• Centers for Disease Control and Prevention. (2023). Heart disease facts and statistics. U.S. Department of Health & Human Services. (https://www.cdc.gov/heart-disease/data- research/facts-stats/index.html)

• Pytlak, K. (2023). Personal key indicators of heart disease [Data set]. Kaggle. (https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease)
