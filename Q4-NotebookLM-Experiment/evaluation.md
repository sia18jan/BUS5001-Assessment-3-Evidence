# Q4 – NotebookLM Evaluation

## Evaluation Objective

The NotebookLM output was evaluated for source grounding, factual support, traceability, practical usefulness and the risk of unsupported inference.

A five-claim audit was performed against the three selected sources.

## Claim Audit Results

| Claim | Evaluation | Key Finding |
|---|---|---|
| Climate Change Authority recommended a 62–70% emissions reduction target from 2005 levels by 2035 | SUPPORTED | The selected Climate Change Authority source explicitly states the 62–70% recommendation. |
| Australian Government released the Sustainable Finance Roadmap on 19 June 2024 following consultation in November 2023 | SUPPORTED | The Treasury source explicitly provides the release date and states that the Roadmap was developed following consultation on the Sustainable Finance Strategy. |
| The UN 2030 Agenda was adopted in 2015 and contains 17 SDGs | PARTIALLY SUPPORTED | Adoption in 2015 and the 17 SDGs were explicitly supported. Describing the framework as "non-binding" went beyond the selected source text. |
| Climate Change Authority review described the ACCU scheme as fundamentally sound but needing to evolve | SUPPORTED | The selected Climate Change Authority material explicitly states this finding. |
| Circular economy directly reinforces SDG 9 and SDG 12 | PARTIALLY SUPPORTED | The sources separately discuss circular economy/Net Zero and list SDGs 9 and 12, but they do not explicitly make this direct connection. |

## Summary

Three of the five audited claims were supported by the selected source material, while two were only partially supported because the generated briefing introduced additional interpretation.

The most important issue was not obvious fabrication, but the tendency for a generative system to combine individually supported facts into a broader conclusion that may not itself be explicitly stated by the sources.

## Strengths

NotebookLM demonstrated several useful capabilities:

- rapid synthesis across multiple authoritative sources;
- source citations and traceability;
- structured briefing generation;
- identification of cross-source themes;
- visual organisation through the Mind Map function; and
- support for subsequent source-based fact checking.

## Limitations

The experiment also identified limitations:

- source citation does not guarantee that every interpretation is explicitly supported;
- conceptual synthesis can blur the distinction between evidence and inference;
- high-level webpages may not contain sufficient detail for operational compliance decisions;
- recommendations generated from policy material may represent reasonable inference rather than explicit regulatory requirements; and
- outputs remain dependent on the quality, scope and currency of the selected sources.

## Governance Assessment

NotebookLM is suitable as a decision-support and research-synthesis tool, but it should not be treated as an autonomous authority for regulatory or ESG compliance decisions.

A human-in-the-loop workflow is preferable:

1. select authoritative sources;
2. generate the initial synthesis;
3. inspect source citations;
4. audit material factual claims;
5. distinguish evidence from inference;
6. verify high-impact recommendations against primary regulatory material; and
7. obtain appropriate human approval before organisational action.

## Overall Evaluation

The experiment demonstrates that source-grounded generative AI can improve the speed and structure of ESG research while preserving substantially better traceability than an ungrounded general-purpose response. However, source grounding reduces rather than eliminates hallucination and inference risk.

The strongest use case is therefore augmentation: NotebookLM can accelerate synthesis and knowledge organisation, while human judgement remains responsible for verification, interpretation and final decision-making.
