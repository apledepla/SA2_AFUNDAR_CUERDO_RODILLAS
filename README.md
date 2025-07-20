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

Now, since it was justified that the permutation approach with Glucose have the higehst impact, in the resampling phase, bootstrap and jackknife methods were applied to evaluate the stability, bias, and variance of the glucose coefficient across different model configurations. Both resampling techniques on the Glucose produced low bias and variance, confirming the robustness of glucose as a key predictor. After the Glucose classification, it numerous predictors were added with the key predictor. After adding 2 more variables (BMI and Insulin), it is found out that adding BMI consistently improved the stability of the coefficient by reducing variance, and proved to be the better version than the glucose only. For model validation, bootstrap resampling was also used to assess performance metrics such as accuracy, precision, recall, F1-score, and RMSE. 

Results showed that the Glucose + BMI model achieved the best overall performance, with improved recall and F1-scores compared to models using glucose alone or combined with insulin. This indicates that while glucose remains the strongest individual predictor, the inclusion of BMI leads to a more accurate and balanced prediction model for diabetes risk.

## Scope and Limitations

This study aims to explore and identify the most significant clinical predictors of diabetes using the Pima Indians Diabetes Dataset, which includes performing exploratory data analysis, visualizing variable distributions, and applying statistical inference techniques such as bootstrap, jackknife, permutation testing, and Bayesian inference. The dataset provides eight health-related features and one binary outcome. All analysis will be conducted using R. However, several limitations are needed to be acknowledged:
    Several features contain zero values that likely represent missing data. 
    The dataset also only includes female patients of Pima Indian descent, limiting the scope into female patients who are pregnant and generalization of findings to broader populations. 
    The dataset is cross-sectional, lacking any temporal information (e.g., disease progression or patient follow-up).

Finally, the scope of the analysis is restricted to basic and intermediate statistical methods due to the academic nature of the project, and does not include advanced machine learning techniques. Thus, it is important to interpret these results within the context of these limitations.


## Conclusion

Based on the overall comprehensive statistical analysis, several conclusion can be drawin regarding the primary predictors of diabetes risk among women in pregnancy. In both the permutation testing and Bayesian inference, it was consistently identified Glucose as the main driving factor in the probability of diabetes,  with BMI serving as an important secondary contributor. This conclusion is further supported by the bootstrap and jackknife resampling analyses, which confirmed the stability and low bias of the glucose coefficient, especially when combined with BMI, indicating a strong and consistent relationship.

For the distribution of key variables, exploratory data analysis revealed several predictors, e.g. Glucose, BMI, and Insulin, showed skewed distribution. Further backed by the KS tests. By this, it thus shows that the binary outcome variable aligned with a binomial distribution, validating the application of logistic regression for classification modeling.

In finalizing the report, the analyses established that through effective resampling techniques, it shows that the Glucose + BMI model consistently demonstrated as the best predictive model, reaching up to 76.32% accuracy rating. And with better evaluation to accuracy, recall, and F1-scores, it offers the most balanced prediction among all the models. Based on the logistic regression models, each one-unit increase in Glucose is associated with approximately a 3.7% increase in the odds of developing diabetes, as indicated by the coefficient (~0.038). This effect was consistent across resampling methods and remained the strongest predictor of diabetes risk.

In summary, the analysis establishes that Glucose is the strongest and most consistent predictor of diabetes risk, with BMI improving model performance without adding significant complexity. Through effective resampling techniques, it helped reduced the overfitting and addressed a concern of having a smaller dataset. These conclusions directly address the research questions by identifying key predictors, confirming variable distributions, and validating model performance through resampling strategies.

## Future Exploration Ideas

To address the limitations of the study, future research could consider the following:
  Data Imputation Techniques - To replace the missing values from the dataset into values that represent the entire dataset for better representation and analysis
  
  Broader dataset - Since the current study only focused on female & pregnant patiets on Pima Indians, future research can broaden the dataset that include other participants such as other genders, ethnicities and groups.
  
  Model Validation - This is to cross-validate the preliminary model used to create a robust and accurate representation of the dataset.
