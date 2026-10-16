# Q3 – LLM Classification Prompt

## Experiment Purpose

The LLM was tested as a zero-shot classifier for organisational ESG and sustainability incident messages. The objective was to determine whether the model could classify the issue, assess urgency, identify follow-up requirements and recommend an appropriate organisational team while returning a consistent structured output.

## Prompt

Classify the following organisational sustainability incident message.

Return ONLY valid JSON using exactly this schema:

{
  "issue_category": "",
  "urgency": "",
  "sentiment": "",
  "followup_required": "",
  "recommended_team": "",
  "escalation_reason": "",
  "data_sensitivity_risk": "",
  "brief_summary": ""
}

Rules:

- issue_category must identify the sustainability issue represented by the message.
- urgency must be LOW, MEDIUM, HIGH, or CRITICAL.
- sentiment must describe the overall sentiment of the message.
- followup_required must be Y or N.
- CRITICAL should only be used when the message indicates an immediate threat to human safety, severe environmental harm, or major operational disruption requiring urgent escalation.
- recommended_team must identify the most appropriate organisational team based only on the information provided.
- escalation_reason must briefly explain why escalation is or is not required.
- data_sensitivity_risk must assess whether the message presents a meaningful information-sensitivity risk.
- brief_summary must contain a concise factual summary based only on the message.
- Do not invent facts that are not contained in the message.

## Test Message 1

"There is a water leak in Building C that has been running all morning."

## Test Message 2

"The air conditioning and lights on Level 4 have been left running every night this week even though the office is empty."

## Test Message 3

"There is exposed electrical wiring beside the leaking water in the staff kitchen and someone nearly slipped. Please get someone here immediately."

## Experimental Design

The same classification rules and JSON schema were retained across all three tests. Only the incident message was changed. This allowed the experiment to assess whether the LLM responded appropriately to differences in issue type, recurrence and safety severity.
