# POP score calculator

Web calculator for the Palliative-Oncologic Prognostic (POP) score, a prognostic model for outpatients with advanced cancer referred to palliative care (Cox model with seven clinical variables).

The calculator returns the predicted survival probability at 1, 3, 6 and 12 months with approximate 95% confidence intervals. It runs entirely in the browser: no patient data are stored or transmitted.

## Use
Open `index.html` in a browser, or serve the repository with GitHub Pages.

## Model
- Variables: number of metastatic sites (1 vs ≥2), histology group, peripheral oedema, clinical prognostic category (>3, 1-3, <1 month), ECOG performance status, liver metastases, systemic anticancer therapy within 30 days before referral, and the histology × oedema interaction.
- Survival: S(t | x) = S0(t)^exp(LP), with Breslow baseline survival S0 at 1, 3, 6 and 12 months.
- Confidence intervals: bootstrap (500 resamples of the development cohort, Cox model and Breslow baseline refitted), on the complementary log-log scale. They do not account for optimism or model selection.

## Status
Research tool. Developed retrospectively in a single centre (n = 709, 608 deaths) with internal validation only. Not externally validated and not intended to guide individual clinical decisions.

## Citation
Massa G, et al. Manuscript in preparation. See `CITATION.cff`.

## Licence
MIT, see `LICENSE`.
