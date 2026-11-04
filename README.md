# Multivariate OLS — What “Controlling For” Actually Does

## Objective

I used simulated data to study how controls, omitted variables, interactions, and multicollinearity change the meaning of regression coefficients.

## Methodology

- I simulated wages that depended on education and ability.
- I compared regressions that included and omitted ability.
- I checked the omitted-variable-bias formula against the known bias.
- I demonstrated Frisch-Waugh-Lovell by residualizing wages and education.
- I showed how controlling for a common outcome can create a false relationship.
- I calculated variance inflation factors for highly related regressors.
- I fitted an interaction between experience and union membership.
- I checked an AI-generated specification-table function against regressions I had already calculated.

## Key Findings

Leaving ability out produced an estimated return to education of **5,126**, compared with the true effect of **2,500**. Controlling for ability reduced the estimate to **2,546**. The omitted-variable formula predicted a bias of **2,629**, close to the actual bias of **2,626**.

Frisch-Waugh-Lovell produced the same education coefficient as the full regression. In the control example, adding a variable caused by both the treatment and outcome changed a true effect of zero into an estimate of **−0.596**.

Highly related regressors made the standard errors about **12 times larger**, but did not bias their combined estimated effect. In the interaction model, an additional year of experience was worth approximately **$903** for non-union workers and **$504** for union members.

## Conclusion

I found that adding more controls does not automatically make a regression more accurate. Whether a control removes or creates bias depends on the causal relationship among the variables, and interaction terms are necessary when effects differ across groups.
