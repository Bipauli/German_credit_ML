# Mitigating bias in Machine Learning : Application to Credit Scoring

Repository for the final project of the Advanced Machine Learning course (taught by Austin Stromme at ENSAE Paris).

## Project overview
This project explores techniques to mitigate bias in machine learning models, with a specific focus on credit scoring. Using the German Credit Dataset, we evaluate the fairness and performance of various models and implement bias mitigation strategies to improve outcomes for underprivileged groups.

## Dataset

**Dataset:** We used the [German Credit Dataset](https://archive.ics.uci.edu/ml/datasets/statlog+german+credit+data), which contains information on 20 variables and the creditworthiness (Good or Bad) of 1000 loan applicants. This dataset includes attributes like marital status, sex, credit score, loan amount, and housing status. It can be used to study gender disparities in credit decisions.

**Fairness Parameter:** Sex, encoded as a binary variable in the dataset.

**Target Variable:** Creditworthiness (Good or Bad).

## Methods
1. **Bias quantification** : Explore and define fairness metrics in machine learning :
    * **Equalized Odds** : A predictor Ŷ satisfies equalized odds with respect to a protected attribute A and an outcome Y if Ŷ and A are independent given Y. In simpler terms, for a specific outcome (e.g., Good credit), the model should have equal true positive rates across different demographic groups (e.g., male and female). Similarly, for the other outcome (Bad credit), the model should have equal false positive rates.
    Pr{Ŷ = 1 | A = 0, Y = y} = Pr{Ŷ = 1 | A = 1, Y = y}, y ∈ {0,1}

    * **Equal Opportunity** : A relaxation of equalized odds, requiring non-discrimination only within the Good Credit outcome group. For instance, individuals who repay their loans should have equal opportunities to obtain loans, regardless of their demographic group.

    * **Demographic Parity** : A predictor Ŷ satisfies demographic parity if Pr{Ŷ = 1 | A = 0} = Pr{Ŷ = 1 | A = 1}. In other words, the likelihood of a positive outcome should be the same regardless of where an individual is in the protected group (e.g. female).

2. **Baseline models** : Test various binary classification models (logistic regression, random forests, etc.) and evaluate their performance and fairness on the German Credit Dataset.
3. **Debiasing techniques** : Apply and compare various bias mitigation techniques:
   - Reweighting (pre-processing)
   - Reject Option-based Classification (post-processing).


## Authors
* Pauline Bian
* Julia Lu
* Marie Meyer
