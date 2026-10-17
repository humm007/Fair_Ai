# Questionnaire variable map

This map describes constructs in the revised questionnaire. The identifiers below were added for repository navigation. They are not a production dataset schema or confirmed Qualtrics export names.

| Domain | Question IDs | Constructs | Response structure |
|---|---|---|---|
| Household and demographics | Q01–Q08 | Household size; age and gender of members; disability; ethnicity; sexual orientation; religion; marital status; outward postcode | Counts, categorical answers and text |
| Socioeconomic circumstances | Q09–Q14 | Education; income band; employment; working pattern; tenure; residential setting | Categories and a hybrid-working estimate |
| Housing and systems | Q15–Q25 | Dwelling type; area; age; rooms; insulation and glazing; orientation; heating; controls; hot water; ventilation; generation | Categories and room counts |
| Occupancy and behaviour | Q26–Q33 | Presence by time of day; meals; cooking style; visitors; switching lights off; laundry; hot-water use | Time-band responses, counts and categories |
| Lifestyles and practices | Q34–Q41 | Thermal preference; cooling; setpoint; windows; efficient-appliance indicators; cooking fuel; energy attitudes; free text | Categories, temperature and text |

## Roles in the analysis

**Audit information:** demographic and socioeconomic fields can define groups for investigating error patterns. Their collection does not by itself determine which fields should enter a prediction model.

**Physical context:** building fabric, heating and hot-water systems help describe the home in which energy is consumed.

**Occupancy and practice context:** presence, working patterns, cooking and comfort preferences help describe how that home is used.

**Linking the constructs:** a future analysis can investigate group differences alongside building and behavioural context, while keeping its modelling assumptions and causal limitations explicit.

## Data-definition work still needed

Before implementation, each field needs a type, allowed values, unit where relevant, missing-value policy and intended use. Multi-select behaviour, household-member repetition and survey branching should be specified explicitly. See the [revision notes](revision-notes.md) for source-draft limitations and the [evaluation plan](../docs/evaluation-plan.md) for proposed analysis.
