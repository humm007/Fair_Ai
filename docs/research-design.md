# Research design

## Purpose

Investigate how household circumstances, occupant behaviour and demographic or socioeconomic characteristics relate to household energy-use patterns, and how those relationships could inform the assessment of prediction fairness.

The academic project outline frames this as a technical and legal research question about potential discrimination in household energy prediction. The public documentation treats unequal error as a question to investigate. It does not establish discriminatory effects or make a legal determination.

## Working research questions

1. Which household, building and behavioural variables are needed to describe differences in energy-use patterns?
2. How do those patterns vary across demographic and socioeconomic groups?
3. Would models using richer household and behavioural information have different error patterns from simpler baselines?
4. Which findings would depend on the assumptions used to simulate consumption?

The first two questions reflect the supplied project rationale. The model-comparison and evaluation questions are proposed extensions for a future empirical stage.

## Proposed stages in the project outline

### 1. Questionnaire-based data collection

The outline proposes a Qualtrics survey with a target of 2,000 UK participants, recruited through social-media channels. The instrument connects household and demographic information, socioeconomic circumstances, building characteristics and occupant behaviour.

That target describes the intended survey. No participant responses or achieved sample size are included in this repository. A sampling and study-approval process would be needed before fieldwork.

### 2. Energy-use estimation

The outline proposes thermodynamic and simulation models to estimate energy-use patterns from household and behavioural information. Housing characteristics and weather conditions affect those estimates and would need to be specified in an implemented workflow.

Simulation outputs would depend on model assumptions. Any future result should state clearly whether its target is measured energy consumption or a simulated estimate. Validation against simulated labels alone would establish agreement with that simulator, rather than performance against real billing outcomes.

### 3. Association analysis

The outline proposes examining relationships between energy-use patterns and protected or socioeconomic characteristics, including an entropy-based class measurement. The exact operational definition and implementation of that measurement still need to be specified.

Association analysis can identify patterns to investigate. It does not establish causation or determine that a model's decisions are unlawful.

### 4. Prediction-model development

The outline proposes subsequent development of a fairness-aware prediction model. Model families, training code, fitted parameters and performance results are not supplied in the source folder.

The [proposed evaluation plan](evaluation-plan.md) describes how a future empirical stage could compare model variants and assess errors across groups.

## Why these questionnaire domains?

| Domain | Design rationale |
|---|---|
| Household composition | Energy needs depend partly on who lives in the home and how many people are present |
| Demographic characteristics | Defined group information is needed to investigate differences between groups |
| Socioeconomic circumstances | Income, employment and tenure describe circumstances that can shape choices and constraints |
| Building characteristics | Floor area, age, insulation, heating and ventilation influence demand independently of household routines |
| Occupancy and practices | Working patterns, presence, cooking, laundry and comfort preferences describe how the building is used |

These are candidate research constructs. Their presence in a questionnaire does not itself establish predictive value or fairness. The [variable map](../questionnaire/variable-map.md) records the available fields, and the [revision notes](../questionnaire/revision-notes.md) identify unresolved measurement issues.

## Literature and the scope of novelty

The [reading list](../references/reading-list.md) includes existing research on socioeconomic, building and behavioural influences on energy use. The study's potential contribution is its particular research design and fairness question. A complete literature review would be needed to establish its novelty.

## Attribution

Jabed drafted the initial questionnaire. Academic leads refined and finalised it. This document summarises the supplied academic outline and the questionnaire drafts; it is a portfolio explanation, not a published study protocol or evidence that the empirical stages have been completed.
