# Household-Income-Analysis
Factors Affecting Household Income in the  Northern Midlands and Mountains in Vietnam

## Overview
This project analyzes the factors influencing household income in the Northern Midlands and Mountains of Vietnam. Using a dataset of 7,417 households across 14 provinces, I apply Ordinary Least Squares (OLS) regression in Stata to assess the impact of key socioeconomic factors.
* Key Variables:

Explanatory: Age, education, gender, marital status, ethnicity, household size, land types, urban/rural classification.

Dependent: Household income per capita (log-transformed).

## Goal of this notebook
1. Analyze the proportional income differences among groups
2. Compare income differences between provinces
3. Assess how different types of land (annual cropland, perennial cropland, forestland, garden land) affect household income
4. Use standardized coefficients to compare the relative influence of each independent variable on income
5. Test the alternative hypothesis that the effect of education on income
6. Analyze the quadratic relationship between age and income

## Methodology: Ordinary Least Squares (OLS) Regression
The model is defined as:
![image](https://github.com/user-attachments/assets/c8aa5801-2fca-45c1-a881-e3abda2f340c)

### OLS Assumptions and Tests
1. Linearity in Parameters: Our model satisfied this assumption. 

2. Random Sampling: The data is a random sample drawn from the population. It means that every member of the population has an equal chance of being selected for the sample. 

3. No Perfect Multicollinearity: All VIF values below 10 as a rule of thumb, indicating that the regression model has no perfect multicollinearity and the coefficient estimates are considered reliable.  

![image](https://github.com/user-attachments/assets/592f1d5c-63f2-40ed-a6a8-664d76ba113a)

4. Zero Conditional Mean: To detect whether our model is violating variable omission errors, we conducted the Ramsey reset test. 

![image](https://github.com/user-attachments/assets/6ef10d6c-10cb-4530-89f7-6017ef7c29b9)

p-value of 0.0000 means that the result is statistically significant -> Reject H0

5. Homoscedasticity: The homogeneity of variance (homoscedasticity) assumption in the regression model's error terms is tested using the Breusch-Pagan/Cook-Weisberg test. 

The model meets Heteroscedasticity. After that, I used Log transformation to adjust for heteroskedasticity in this model. 

![image](https://github.com/user-attachments/assets/7eb90a54-c648-4a6c-a28b-9d4d4008d4d1)

p-value = 0.4758 > 0.05 -> do not reject H0 

The new model does not violate the assumption of heteroscedasticity, indicating that the model has more precisely and successfully addressed the issue. 

6. Normality: Residuals should follow a normal distribution with zero mean and constant standard deviation. I used Q-Q plots to test the model.

![image](https://github.com/user-attachments/assets/1e825014-e537-4dcc-861b-7fcd10051ea4)

The plot shows that the model satisfies the above assumption.  

## Key Findings




