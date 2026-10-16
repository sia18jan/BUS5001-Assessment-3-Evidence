# Q3 – Baseline Comparison

## Purpose

A deterministic rule-based baseline was compared with the LLM classification approach. The purpose was to determine whether the LLM provided additional contextual reasoning beyond simple keyword matching.

## Baseline Method

The baseline uses predefined keywords and rules:

- "water leak", "leaking water", "burst pipe" → WATER_LEAK
- "lights", "air conditioning", "electricity", "energy" → ENERGY_WASTE
- Explicit safety terms such as "exposed electrical", "injury", "danger", "nearly slipped" or "immediately" → escalate urgency
- Repeated or ongoing incidents → follow-up required

Unlike the LLM, the baseline does not interpret broader meaning beyond the predefined rules.

## Comparison Results

| Test | Baseline Classification | LLM Classification | LLM Urgency | Comparison |
|---|---|---|---|---|
| Ongoing water leak | WATER_LEAK | WATER_LEAK | HIGH | Both identified the explicit issue. The LLM additionally produced a contextual explanation for follow-up and urgency. |
| Recurring energy waste | ENERGY_WASTE | ENERGY_WASTE | MEDIUM | Both identified energy waste. The LLM interpreted repeated nightly occurrence while distinguishing it from an immediate emergency. |
| Water + electrical + near-slip risk | WATER_LEAK + safety trigger | WATER_LEAK | CRITICAL | The baseline required explicit safety-trigger rules. The LLM combined multiple contextual risk indicators and explained why immediate escalation was required. |

## Strengths of the Baseline

The deterministic baseline is:

- transparent;
- inexpensive to execute;
- predictable;
- easy to audit; and
- appropriate when categories and vocabulary are tightly controlled.

## Limitations of the Baseline

Its performance depends heavily on predefined words and phrases. Alternative wording, ambiguous descriptions or combinations of risks may require additional manually defined rules. The baseline therefore becomes more difficult to maintain as the variety of incident descriptions increases.

## Strengths of the LLM

The LLM demonstrated stronger contextual interpretation. Most notably, the third test contained several interacting signals: leaking water, exposed electrical wiring, a near-slip event and a request for immediate assistance. The LLM combined these signals and classified urgency as CRITICAL while explaining the immediate human-safety risk.

The LLM also generated a structured summary, recommended organisational team, follow-up decision and escalation rationale without requiring a separate explicit keyword rule for every output field.

## Limitations of the LLM

The LLM is probabilistic rather than deterministic. Outputs can vary, and plausible explanations are not automatically guaranteed to be correct. Consequently, high-impact classifications should not be actioned without appropriate validation and human oversight.

## Overall Comparison

The experiment indicates that the deterministic baseline is preferable when transparency, low cost and predictable keyword matching are the primary requirements. The LLM is more useful when classification depends on context, interacting risk signals and natural-language variation.

For organisational deployment, a hybrid architecture is preferable: deterministic controls can handle clear rules and validation, while an LLM can provide contextual classification and reasoning. Critical or uncertain cases should remain subject to human review.
