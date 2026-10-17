# Proposed evaluation plan

**Status: a proposed next-stage protocol, prepared for this repository in October 2026.** It extends the study outline and has not been implemented or validated in the supplied materials.

## 1. Define the prediction task

Specify the target quantity, unit and time interval before choosing metrics. Examples might be household electricity use over a defined period or a simulation-derived demand estimate. Keep measured and simulated targets distinct throughout the analysis.

Record which inputs would be available when a real prediction is made. Variables used only for a fairness audit should be distinguished from inputs permitted in a deployed predictor.

## 2. Establish the analysis population

Define the intended population, sampling approach and inclusion criteria. Report the number of responses, exclusions, missing fields and observations in each analysed group. A social-media sample needs an explicit assessment of its coverage and selection limitations.

Treat unanswered questions, “prefer not to say” and “don't know” as different response types where appropriate. Define any aggregation of small groups before inspecting their error results. Avoid conclusions for groups with too few observations to support them.

## 3. Construct baselines and comparisons

| Proposed comparison | Question it would test |
|---|---|
| Constant or mean baseline | Does the fitted model improve on a simple reference? |
| Basic household / building model | What can be predicted from a limited description? |
| Additional occupancy and behaviour fields | Does richer information change overall or group-level error? |
| Removal of one questionnaire domain at a time | Which domains contribute useful information? |

Demographic information has a role in defining audit groups. Whether individual variables belong in model inputs requires a separate task-specific decision; collecting them does not automatically justify their use in prediction.

## 4. Prevent evaluation leakage

- Partition observations before fitting imputers, encoders or feature-selection steps.
- Fit preprocessing on training data within each cross-validation fold.
- Keep records from the same household together if there are repeated observations.
- Use temporal or geographic holdouts when those match the generalisation claim.
- Reserve a test set for final evaluation; choose model settings using training and validation data.

These steps are proposed safeguards. They are not assertions about experiments already carried out in this project.

## 5. Report errors at two levels

| Level | Proposed reporting |
|---|---|
| Overall | Mean absolute error and root mean squared error, with the target's unit |
| By group | Group size, mean absolute error and mean signed error, with uncertainty estimates |
| By context | Errors across relevant housing and occupancy settings |
| Across model variants | Changes in error from adding or removing questionnaire domains |

Mean signed error can reveal a tendency to overpredict or underpredict for a group; absolute error describes its magnitude. Report both rather than treating one metric as a complete definition of fairness. Choose any fairness criteria to match the intended use and the people affected.

## 6. Test dependence on simulation assumptions

If targets come from a simulator, vary assumptions such as occupancy schedules, thermal comfort preferences and building characteristics. Check whether group differences are stable under those variations. Report simulator limitations and state what independent measured-data validation would still be required.

## 7. Make the eventual analysis reviewable

An implemented stage should record the data dictionary, preprocessing, split definitions, model settings, random seeds, group definitions and limitations. Results should be traceable to those choices. Any shared examples should use material suitable for public release.

## Decision criteria

A convincing result would identify what was predicted, for whom, against which baseline and under which assumptions. A lower aggregate error alone would not establish that error disparities had improved or that the system was appropriate for a billing use case.
