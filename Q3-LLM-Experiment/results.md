# Q3 – LLM Experiment Results

## Test 1 – Ongoing Water Leak

### Input
"There is a water leak in Building C that has been running all morning."

### LLM Output

```json
{
  "issue_category": "WATER_LEAK",
  "urgency": "HIGH",
  "sentiment": "NEGATIVE",
  "followup_required": "Y",
  "recommended_team": "Facilities/Maintenance",
  "escalation_reason": "Prompt action is required because the water leak has been ongoing all morning, but no immediate threat to human safety, severe environmental harm, or major operational disruption is stated.",
  "data_sensitivity_risk": "LOW",
  "brief_summary": "A water leak in Building C has been running all morning."
}
```

### Interpretation
The model identified the explicit water-leak category and assigned HIGH urgency because the incident was ongoing and required prompt action, while distinguishing it from an immediate critical safety emergency.

---

## Test 2 – Recurring Energy Waste

### Input
"The air conditioning and lights on Level 4 have been left running every night this week even though the office is empty."

### LLM Output

```json
{
  "issue_category": "ENERGY_WASTE",
  "urgency": "MEDIUM",
  "sentiment": "NEGATIVE",
  "followup_required": "Y",
  "recommended_team": "Facilities/Maintenance",
  "escalation_reason": "Follow-up is required because unnecessary energy use has occurred repeatedly throughout the week, but no immediate safety threat or major operational disruption is indicated.",
  "data_sensitivity_risk": "LOW",
  "brief_summary": "Air conditioning and lights on Level 4 have been left running every night this week while the office is empty."
}
```

### Interpretation
The model recognised repeated unnecessary electricity consumption as ENERGY_WASTE but appropriately differentiated the recurring sustainability issue from an immediate emergency.

---

## Test 3 – Critical Safety Context

### Input
"There is exposed electrical wiring beside the leaking water in the staff kitchen and someone nearly slipped. Please get someone here immediately."

### LLM Output

```json
{
  "issue_category": "WATER_LEAK",
  "urgency": "CRITICAL",
  "sentiment": "NEGATIVE",
  "followup_required": "Y",
  "recommended_team": "Facilities/Maintenance",
  "escalation_reason": "Immediate escalation is required because exposed electrical wiring is beside leaking water and a person nearly slipped, indicating an immediate human safety risk.",
  "data_sensitivity_risk": "LOW",
  "brief_summary": "Leaking water is beside exposed electrical wiring in the staff kitchen, and someone nearly slipped."
}
```

### Interpretation
The model escalated the incident from a normal water-leak classification to CRITICAL after contextual safety information was introduced. This demonstrates sensitivity to risk context rather than classification based solely on the issue keyword.

## Overall Result

Across the three tests, the LLM maintained the requested structured schema and differentiated between recurring sustainability problems and immediate safety hazards. The strongest contextual reasoning was demonstrated in Test 3, where the combination of water, exposed electrical wiring and a near-slip event resulted in CRITICAL urgency.
