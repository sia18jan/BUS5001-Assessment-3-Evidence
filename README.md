# BUS5001 Assessment 3 – Experiment Evidence

This repository contains experiment logs, prompts, outputs, comparison evidence and screenshots supporting BUS5001 Assessment 3, particularly Questions 3 and 4.

## Q3 – LLM Classification Experiment

The Q3 experiment evaluates a large language model for classifying and triaging organisational ESG and sustainability incident messages.

Evidence is contained in the `Q3-LLM-Experiment` folder.

### Included Evidence

- `prompt.md` – LLM prompt, JSON schema, classification rules and test messages.
- `results.md` – structured outputs from the three LLM test scenarios.
- `experiment-log.md` – experiment design, observations and findings.
- `baseline-comparison.md` – comparison between the LLM and a deterministic rule-based baseline.
- `q3-critical-test.png` – screenshot evidence of LLM testing.
- `q3-critical-testb.png` – additional screenshot evidence showing classification outputs.

### Q3 Test Scenarios

1. Ongoing water leak – HIGH urgency.
2. Recurring energy waste – MEDIUM urgency.
3. Water leak with exposed electrical wiring and near-slip risk – CRITICAL urgency.

The experiments demonstrate how contextual information changes classification and escalation decisions compared with simple keyword-based rules.

---

## Q4 – NotebookLM Source-Grounded Experiment

The Q4 experiment evaluates NotebookLM for source-grounded ESG policy research, synthesis, factual verification and visual knowledge organisation.

Evidence is contained in the `Q4-NotebookLM-Experiment` folder.

### Source Set

The experiment used three authoritative sources:

1. United Nations – Sustainable Development Goals.
2. Australian Government Climate Change Authority.
3. Australian Treasury – Sustainable Finance Roadmap.

### Included Evidence

- `experiment-log.md` – experiment design, source set, activities and findings.
- `prompts.md` – prompts used for the policy briefing, factual claim audit and mind-map experiment.
- `evaluation.md` – evaluation of source grounding, factual support, inference risk and governance implications.
- Screenshot evidence – NotebookLM source selection, prompt, generated briefing and mind map.

### Q4 Experiments

1. Source-grounded ESG policy briefing.
2. Five-claim factual audit against the selected sources.
3. Visual mind map of global sustainability and Australian climate-policy frameworks.

The evaluation found that source-grounded generative AI can improve research speed and traceability, but human verification remains necessary where generated outputs introduce interpretation or inference.

---

## Repository Purpose

This repository provides supporting experimental evidence for the written BUS5001 Assessment 3 submission. The assessment report contains the full analysis and discussion; this repository provides reproducible supporting evidence for Q3 and Q4.
