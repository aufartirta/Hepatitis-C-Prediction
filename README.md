# Predicting Hepatitis-C Patients with Machine Learning Algorithms
## Project Overview
### Objective:
The objective of this project is to leverage machine learning techniques and data analysis to uncover key patterns and develop predictive models for Hepatitis C, using the UCI Machine Learning Hepatitis C dataset. The analysis aims to identify significant biomarkers associated with the disease and determine the most effective machine learning models for predicting Hepatitis C status.

### Data Source:
This project utilizes the Hepatitis C dataset from the [UCI Machine Learning Repository.](https://archive.ics.uci.edu/dataset/571/hcv+data). The dataset includes demographic information, biochemical laboratory test results, and attributes related to Hepatitis C status.

### Dataset Description:
The dataset consists of several key features:
* Demographic Information: Age, gender, and other personal data.
* Biochemical Lab Results: Levels of various liver enzymes and biomarkers, such as AST, ALP, ALT, ALB, BIL, ACHe, and GGT.
* Hepatitis C Virus (HCV) Features: Indicators of Hepatitis C infection status and disease progression.
* Target Variable: Hepatitis C status, categorized into multiple stages, including fibrosis and cirrhosis.

## Key Findings:
1. Biomarker Correlations:
   * AST (Aspartate Aminotransferase): Shows a strong positive correlation (0.62) with disease severity. Higher AST levels are associated with more advanced stages of Hepatitis C.
   * BIL (Bilirubin): Displays a moderate positive correlation (0.40) with the disease, indicating that higher BIL levels are also linked to more severe cases.
   * GGT (Gamma-Glutamyl Transferase): Exhibits a moderate positive correlation (0.44) with disease progression, suggesting that elevated GGT levels correspond with more advanced Hepatitis C stages.
2. Gender Distribution:
   * Frequency: The dataset shows that male patients are more frequently diagnosed with Hepatitis C than female patients, highlighting potential gender-related differences in disease prevalence.
3. Implications of Biomarker Levels:
   * Higher AST, GGT, and BIL Levels: Patients with elevated levels of AST, GGT, and BIL are more likely to have advanced stages of Hepatitis C, making these biomarkers critical for disease monitoring and management.

## Machine Learning Models and Results:
To predict Hepatitis C status, several machine learning models were implemented and evaluated based on their accuracy and F1-score. These metrics are critical in assessing the model’s ability to correctly classify patients with and without Hepatitis C, as well as its performance in balancing precision and recall.

1. Logistic Regression (LR):
   * Accuracy: 0.90
   * F1-Score: 0.70
   * Interpretation: Logistic Regression provides a solid baseline model with high accuracy but relatively lower F1-score, indicating it may struggle with classifying minority classes effectively.

2. Random Forest (RF):
   * Accuracy: 0.95
   * F1-Score: 0.75
   * Interpretation: The Random Forest model significantly improves both accuracy and F1-score, indicating a better overall performance in classifying patients correctly, with a strong balance between precision and recall.

3. Gradient Boosting (GB):
   * Accuracy: 0.93
   * F1-Score: 0.80
   * Interpretation: Gradient Boosting achieves the highest F1-score, making it the best model for balancing precision and recall. It also offers robust accuracy, making it a strong candidate for predictive tasks in Hepatitis C classification.

4. Support Vector Machine (SVM):
   * Accuracy: 0.90
   * F1-Score: 0.70
   * Interpretation: The SVM model mirrors the performance of Logistic Regression, with high accuracy but a moderate F1-score, suggesting similar challenges in classifying minority classes.

## Conclusions:
1. Model Selection: Gradient Boosting is recommended as the primary model for predicting Hepatitis C status due to its strong balance of accuracy and F1-score. Random Forest also performs well and can be a reliable alternative, particularly for applications that prioritize overall accuracy.
2. Role of Biomarkers: The strong correlations between AST, GGT, BIL, and disease severity underscore the importance of these biomarkers in monitoring Hepatitis C progression. These biomarkers can be used as key features in predictive models and clinical decision-making.
3. Gender Considerations: The higher frequency of Hepatitis C among males suggests that gender-specific factors may influence disease prevalence and should be considered in both clinical practice and future research.

## Next Steps:
1. Model Deployment: Consider deploying the Gradient Boosting model in clinical settings to assist healthcare providers in the early detection and management of Hepatitis C.
2. Further Exploration: Investigate the underlying reasons for the gender disparity in Hepatitis C prevalence and explore additional biomarkers that could improve model performance.
3. Patient Monitoring: Use the identified correlations between biomarkers and disease severity to develop tools for ongoing patient monitoring and personalized treatment plans.
