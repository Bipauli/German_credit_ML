# German_credit_ML
## Dataset

**Dataset:** We will use the German Credit Data, which contains information on 20 variables and the creditworthiness (Good or Bad) of 1000 loan applicants. This dataset includes attributes like marital status, sex, credit score, loan amount, and housing status. It can be used to study gender disparities in credit decisions.

**Fairness Parameter:** Sex, encoded as a binary variable in the dataset.

**Target Variable:** Creditworthiness (Good or Bad).

**Baseline Models:** We will test various binary classification models (logistic regression, random forests, etc.) to maximize classification performance.

## Bias Quantification

**Equalized Odds and Equal Opportunity:**

**Equalized Odds:** A predictor Ŷ satisfies equalized odds with respect to a protected attribute A and an outcome Y if Ŷ and A are independent given Y. In simpler terms, for a specific outcome (e.g., Good credit), the model should have equal true positive rates across different demographic groups (e.g., male and female). Similarly, for the other outcome (Bad credit), the model should have equal false positive rates.

Pr{Ŷ = 1 | A = 0, Y = y} = Pr{Ŷ = 1 | A = 1, Y = y}, y ∈ {0,1}

**Equal Opportunity:** A relaxation of equalized odds, requiring non-discrimination only within the Good Credit outcome group. For instance, individuals who repay their loans should have equal opportunities to obtain loans, regardless of their demographic group.

## Debiasing Techniques

**Debiasing Techniques:** We will employ in-processing and/or post-processing techniques to mitigate bias.
