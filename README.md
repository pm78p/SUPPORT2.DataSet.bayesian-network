# Bayesian Network for Predicting Functional Disability in Critically Ill Patients

## Overview
This project utilizes a Bayesian Network to predict functional disability in critically ill patients using the SUPPORT dataset. The SUPPORT dataset contains comprehensive information on 9105 critically ill patients collected from five US medical centers between 1989 and 1994.

## Dataset
The SUPPORT dataset includes various types of variables:
- **Demographic Variables**: Age, Sex, Race.
- **Physiological Measurements**: Mean Blood Pressure (meanbp), White Blood Cell Count (wblc), Heart Rate (hrt), Respiration Rate (resp), Temperature (temp), Creatinine Level (crea), Sodium Level (sod).
- **Disease Severity and Related Variables**: Disease Group (dzgroup), Disease Class (dzclass), Number of Comorbidities (num.co).
- **Survival Estimates**: Estimates of survival at 2 months (surv2m) and 6 months (surv6m).
- **Health Conditions**: Diabetes (diabetes), Dementia (dementia), Cancer (ca).
- **Target Variable**: Functional Disability (sfdm2).

## Data Preprocessing
1. **Cleaning**: Removed columns with more than 1000 missing values and irrelevant identifiers.
2. **Discretization**: Employed quantile-based discretization for continuous variables, using Sturges' formula to determine the number of bins.

## Bayesian Network Construction
- Initial Bayesian Network was drawn based on the intuition of feature characteristics.
- **Estimators**:
  - **Bayesian Maximum Likelihood Estimator (MLE)**: Focuses on the likelihood of observed data.
  - **Bayesian Priors**: Utilized Dirichlet priors and the Bayesian Dirichlet equivalent uniform (BDeu) score for structure learning.

## Methodologies
- **Hill Climbing**: Started with a simple model and iteratively refined it by exploring adjacent solutions.
- **Expectation-Maximization (EM)**: An iterative method to find maximum likelihood estimates of parameters in models with latent variables, particularly useful for incomplete data. This method provided comparable accuracy (valid_acc=64%) to the Bayesian estimator.

## Problems Encountered
- Finding appropriate datasets.
- Dealing with textual and visually complex features.
- Handling datasets with similar feature distributions leading to uniform conditional probability tables (CPTs).
- Repeated data cleaning, preprocessing, Bayesian network drawing, and CPT derivation (7-9 iterations).

## Results
The Bayesian Network and its associated methods successfully modeled the prediction of functional disability in critically ill patients, achieving a validation accuracy of 64%.

## Conclusion
This project demonstrates the application of Bayesian Networks in predicting patient outcomes in a clinical setting, highlighting the challenges and methodologies involved in handling complex medical data.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Contact
For any questions or comments, please contact Mohammad Pourtaheri.
