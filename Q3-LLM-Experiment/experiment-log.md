# Q3 – LLM Experiment Log

## Purpose
This experiment evaluates the use of a large language model for classifying and triaging organisational ESG and sustainability incident messages.

## Output Schema
The LLM was instructed to return structured JSON containing:

- issue_category
- urgency
- sentiment
- followup_required
- recommended_team
- escalation_reason
- data_sensitivity_risk
- brief_summary

## Experiment 1 – Ongoing Water Leak

### Input
"There is a water leak in Building C that has been running all morning."

### Result
- Issue category: WATER_LEAK
- Urgency: HIGH
- Sentiment: NEGATIVE
- Follow-up required: Y
- Recommended team: Facilities/Maintenance
- Data sensitivity risk: LOW

### Observation
The model correctly identified the water-leak category and treated the prolonged incident as requiring prompt follow-up, while not classifying it as an immediate critical safety emergency.

## Experiment 2 – Energy Waste

### Input
"The air conditioning and lights on Level 4 have been left running every night this week even though the office is empty."

### Result
- Issue category: ENERGY_WASTE
- Urgency: MEDIUM
- Sentiment: NEGATIVE
- Follow-up required: Y
- Recommended team: Facilities/Maintenance
- Data sensitivity risk: LOW

### Observation
The model differentiated recurring resource wastage from an immediate emergency and assigned medium urgency.

## Experiment 3 – Critical Safety Context

### Input
"There is exposed electrical wiring beside the leaking water in the staff kitchen and someone nearly slipped. Please get someone here immediately."

### Result
- Issue category: WATER_LEAK
- Urgency: CRITICAL
- Sentiment: NEGATIVE
- Follow-up required: Y
- Recommended team: Facilities/Maintenance
- Data sensitivity risk: LOW

### Observation
The model recognised the interaction between leaking water, exposed electrical wiring and a near-slip event as an immediate human-safety risk requiring escalation.

## Baseline Comparison

A deterministic keyword baseline was used for comparison. It maps explicit terms such as "water leak" to WATER_LEAK and terms such as "lights", "air conditioning" and "energy" to ENERGY_WASTE. Safety terms such as "exposed electrical", "danger", "injury" and "immediately" trigger escalation.

The baseline is transparent, deterministic and inexpensive but depends on predefined vocabulary. The LLM demonstrated greater contextual reasoning, particularly when multiple risk signals appeared together. However, LLM outputs require validation because generative systems may produce inconsistent or unsupported classifications.

## Purpose
This experiment evaluates the use of a large language model for classifying and triaging organisational ESG and sustainability incident messages.

## Output Schema
The LLM was instructed to return structured JSON containing:

- issue_category
- urgency
- sentiment
- followup_required
- recommended_team
- escalation_reason
- data_sensitivity_risk
- brief_summary

## Experiment 1 – Ongoing Water Leak

### Input
"There is a water leak in Building C that has been running all morning."

### Result
- Issue category: WATER_LEAK
- Urgency: HIGH
- Sentiment: NEGATIVE
- Follow-up required: Y
- Recommended team: Facilities/Maintenance
- Data sensitivity risk: LOW

### Observation
The model correctly identified the water-leak category and treated the prolonged incident as requiring prompt follow-up, while not classifying it as an immediate critical safety emergency.

## Experiment 2 – Energy Waste

### Input
"The air conditioning and lights on Level 4 have been left running every night this week even though the office is empty."

### Result
- Issue category: ENERGY_WASTE
- Urgency: MEDIUM
- Sentiment: NEGATIVE
- Follow-up required: Y
- Recommended team: Facilities/Maintenance
- Data sensitivity risk: LOW

### Observation
The model differentiated recurring resource wastage from an immediate emergency and assigned medium urgency.

## Experiment 3 – Critical Safety Context

### Input
"There is exposed electrical wiring beside the leaking water in the staff kitchen and someone nearly slipped. Please get someone here immediately."

### Result
- Issue category: WATER_LEAK
- Urgency: CRITICAL
- Sentiment: NEGATIVE
- Follow-up required: Y
- Recommended team: Facilities/Maintenance
- Data sensitivity risk: LOW

### Observation
The model recognised the interaction between leaking water, exposed electrical wiring and a near-slip event as an immediate human-safety risk requiring escalation.

## Baseline Comparison

A deterministic keyword baseline was used for comparison. It maps explicit terms such as "water leak" to WATER_LEAK and terms such as "lights", "air conditioning" and "energy" to ENERGY_WASTE. Safety terms such as "exposed electrical", "danger", "injury" and "immediately" trigger escalation.

The baseline is transparent, deterministic and inexpensive but depends on predefined vocabulary. The LLM demonstrated greater contextual reasoning, particularly when multiple risk signals appeared together. However, LLM outputs require validation because generative systems may produce inconsistent or unsupported classifications.
