# nhanes-hypertension-risk-factors
# Risk Factors for Hypertension among US Adults: NHANES 2017-2018

A statistical analysis of hypertension in 5,856 US adults, using the methods from my biostatistics course.

## Question
Which factors (age, BMI, sex, smoking, diabetes, race) go with high blood pressure, and can BMI or waist be used to screen for it?

## Data
NHANES 2017-2018 (CDC). Six files merged on SEQN: DEMO_J, BPX_J, BMX_J, SMQ_J, DIQ_J, BPQ_J. The notebook downloads them directly, so no data files are stored here.
Hypertension = mean systolic >= 130 or diastolic >= 80 or on BP medicine.

## Methods
t-tests, one-way and two-way ANOVA, ANCOVA, repeated measures ANOVA and mixed model, correlation, multiple linear regression, logistic regression, prevalence ratios, ROC analysis, sensitivity analysis.

## Main results
- 54.3% of adults in the sample have hypertension (14% at ages 18-29, 84% at 70-80).
- Age is the strongest factor (adjusted OR 2.02 per 10 years), then BMI, sex and race.
- Raw differences by smoking and diabetes mostly disappear after adjusting for age and BMI.
- BMI and waist are weak screens (AUC 0.62 and 0.67). The full logistic model reaches AUC 0.82.
- The sex difference depends on the cutoff (OR 1.60 with 130/80, 1.09 and not significant with 140/90).

## Limitations
Cross-sectional (association only), no survey weights, one visit, BP medicine lowers measured BP, Hosmer-Lemeshow test significant.

## How to run
Open `Hypertension_NHANES_Analysis.ipynb` in Google Colab and click Runtime, then Run all.
