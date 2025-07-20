# From Data to Diagnosis: Exploring Diabetes Predictors through Bootstrap, Jackknife, and Inference Models


## Group Members & Task Contribution:
Audrie Lex Afundar (Task 4, 5 & 7)
Naomi Hannah Cuerdo (Task 1, 6 & 7)
Christian Miguel Rodillas (Task 2, 3 & 7)

## Dataset Overview
The dataset contains anonymized medical diagnostic measurements of women, including:

Glucose: Plasma glucose concentration

BMI: Body Mass Index

Age: Age in years

Insulin: 2-hour serum insulin levels

Outcome: Diabetes diagnosis (1 = diabetic, 0 = non-diabetic)

## Instructions on how to read:
  Task 1 & 6 contains the introduction of the problem statement, research questions and exploratory data analysis, Task 4 & 5 contains the KS test using Permutation approach as well as the MCMC for Bayesian Inference, Task 2 & 3 contains the jackknife and bootstrap with resampling for model validation. The summary and findings can be seen below the README file. Follow these path for a clear story telling and explanation.


## Summary and Findings

Several key patterns emerged from the exploratory data analysis of the health-related variables in the dataset. Some variables exhibited skewed or non-normal distributions, indicating the potential need for transformation or the use of non-parametric methods. Others followed approximately normal distributions, making them suitable for traditional parametric analyses. Certain variables also showed signs of data quality issues, such as implausible zero values, which may need to be treated as missing data. Additionally, the target variable, diabetes diagnosis, is binary and fits a binomial distribution, confirming the appropriateness of classification models such as logistic regression. Overall, these findings inform data preparation decisions and guide the selection of appropriate statistical techniques for modeling and inference in the subsequent phases of the study. 

It is shown in the KS test using Permutation approach that there are 3 features that have significant effect in the odds of having diabetes. This includes the Glucose, BMI and Insulin with Glucose being the most impactful one. Moreover, Pregnancies have borderline significance but not enough to reject the null hypothesis. On the other hand, the MCMC for Bayesian Inference justified the findings of the permutation approach with Glucose having the highest impact on the odds of having diabetes, followed by the BMI. On the other hand, Pregnancies and BloodPressure had a minimal postive relationship on having diabetes despite being insignificant. There is not enough evidence or confidence to truly accept these effects.

## Scope and Limitation


