# Predictive Classification for Dementia

## Overview  
This project investigates the use of machine learning techniques to identify individuals at high risk of dementia using a mix of demographic, cognitive, and MRI-based features. Traditional diagnosis methods rely on expensive or less accessible tests. Our goal was to design a low-cost, high-recall classifier that could help flag potential dementia cases earlier, enabling timely clinical attention.

## Dataset  
The dataset used was the OASIS Cross-Sectional dataset, filtered to 373 complete entries. It included:
- Clinical Dementia Rating (CDR)
- Mini-Mental State Examination (MMSE)
- MRI-derived volume metrics: nWBV, eTIV, ASF
- Demographic data: age, education, socioeconomic status, gender

## Methodology  
We implemented and compared the following classifiers:
- **Logistic Regression** (with L1 and L2 regularization)
- **Gaussian Naive Bayes**
- **Decision Tree**
- **Random Forest**
- **K-Nearest Neighbors**

Data preprocessing included type-specific imputation, standardization, and correlation analysis. Class imbalance was handled with weighted classification during training.

## Results  
Among all models, Random Forest achieved the best performance:
- **Test Accuracy:** 88%
- **Macro F1-Score:** 0.82
- **Recall on Demented Class:** 96%

CDR, MMSE, and MRI delay emerged as the most predictive features. Brain volume metrics (nWBV, ASF) also contributed meaningfully to final predictions.

## Future Work  
- Test on an external cohort to improve generalizability  
- Try ensemble stacking and additional classifiers (e.g., SVM, XGBoost)  
- Add bootstrap confidence intervals and clinical UI for deployment  
