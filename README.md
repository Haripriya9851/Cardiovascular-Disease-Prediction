# Cardiovascular Disease Risk Prediction  
**Group Project on ML Risk Model for Cardiovascular Disease Prediction**  

## Overview  
Our analysis confirms that age, medical history (COPD, diabetes), lifestyle factors (sleep, smoking, alcohol) significantly impact cardiovascular disease risk, while BMI alone is not a primary predictor.  

## Problem Statement  
Heart disease is the leading cause of death in the U.S., with 697,000 fatalities in 2021 (CDC, 2023). This study analyzes the *Personal Key Indicators of Heart Disease* dataset from Kaggle, based on CDC surveys, to identify key risk factors and inform healthcare interventions.  

## Methodology  
### Exploratory Data Analysis (EDA)  
- Addressed data inconsistencies and visualized relationships between demographics, behaviors, and heart disease.  

### Hypothesis Testing  
- **Age**: Older individuals show a significantly higher risk.  
- **Smoking/Alcohol**: Higher prevalence among affected individuals.  
- **Diabetes**: Strong association with cardiovascular events.  
- **BMI**: Weak correlation, suggesting it isn't a primary predictor.  

### Machine Learning Models  
#### Logistic Regression  
- **Key predictors**: COPD, age, diabetes, arthritis, depressive disorder, and sleep.  
- **Protective factors**: Physical activity and adequate sleep.  
- **BMI & lifestyle habits**: Higher p-values suggest weaker association.  

#### Decision Tree & Random Forest  
- Random Forest captured non-linear interactions, ranking BMI, age, and sleep as top predictors.  
- COPD had lower significance compared to Logistic Regression.  

#### Model Performance  
| Model | Accuracy | Recall | F1-Score |  
|--------|------------|--------|------------|  
| Logistic Regression | 72.12% | **0.76** | **0.73** |  
| Random Forest | 88.03% | 0.071 | 0.1214 |  

- Logistic Regression achieved the best balance between precision and recall, making it ideal for screening high-risk individuals.  

## Key Insights & Recommendations  
- **Early screening**: Target older adults and those with diabetes/COPD.  
- **Lifestyle interventions**: Promote physical activity, balanced diet, and adequate sleep.  
- **Accessibility**: Improve healthcare access in underserved areas for screenings and preventive care.  

## References  
- **CDC (2023).** [Heart Disease Facts & Statistics](https://www.cdc.gov/heart-disease/data-research/facts-stats/index.html)  
- **Pytlak, K. (2023).** [Personal Key Indicators of Heart Disease Dataset - Kaggle](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease)  
