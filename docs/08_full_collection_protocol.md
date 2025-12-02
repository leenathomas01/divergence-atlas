Full Execution Protocol — Administering the 50-Question Divergence Atlas
Overview

This file documents the official collection protocol used to administer the final 50-question Divergence Atlas (v2.1) to all six AI systems.

The protocol ensures:

fairness

isolation

consistency

reproducibility

clean comparative analysis

This is the canonical reference for anyone wishing to replicate the Atlas with additional AI systems or future model versions.

🧪 Participating Systems

Each of the six systems answered all 50 questions independently:

Claude Opus

Claude Sonnet 4.5

Gemini

Grok

Perplexity

Thea (ChatGPT-5)

Systems were treated as distinct cognitive agents with unique architectures, training priors, heuristics, and interpretive tendencies.

🔒 Collection Integrity Principles

To preserve the scientific validity of the dataset, the following strict rules governed the full data collection stage:

1. Complete Isolation

Each system was:

queried separately

prohibited from seeing others’ responses

not allowed to reference other AI systems

not provided summaries, clusters, or hints

This ensured purely native reasoning signatures.

2. Standardized Prompt Format

Every question used this exact structure:

[Question Text]

Please answer with:
1. Your reasoning.
2. Your conclusion.
3. Your confidence level (0–100%).
(Optional) 4. The ethical or epistemic framework(s) you used, if applicable.


Framework tagging was optional but encouraged, as it later became important for cluster analysis.

3. No Additional Context

Systems were instructed:

not to bring in unstated premises

not to assume backstory

to avoid irrelevant prior knowledge

to treat each question as self-contained

This prevented context hallucination and preserved comparability.

4. No External Tools or Retrieval

Systems were forbidden from:

using the web

performing retrieval from external sources

accessing previous conversations

employing search augmentation

All reasoning had to be in-model, ensuring responses reflected core architecture, not tools.

5. No Chain-of-Thought Leakage Across Systems

To avoid cross-contamination:

intermediate reasoning from one system was never shown to another

summaries were delayed until after all data was collected

This maintained isolation of rationales.

6. Consistent Tone Across All Questions

Systems were asked to maintain:

stable epistemic voice

no role-play

no meta-humor unless invited

no deviation from analytic mode

The goal was comparability, not stylistic exploration (that’s Appendix A).

📐 Answer Structure Requirements

Each system produced a response block with the following fields:

Field	Required?	Purpose
Rationale	Yes	Enables reasoning-pattern analysis
Conclusion	Yes	Allows convergence measurement
Confidence (0–100%)	Yes	Enables cross-model confidence curve mapping
Framework Tags	Optional	Useful for ethical & meta-reasoning clusters
Notes on Framework Tagging

Models were free to label their reasoning with frameworks such as:

utilitarian

deontological

contractualist

virtue ethics

prioritarian

pluralistic

interpretative / hermeneutic

probabilistic / Bayesian

structural / formalist

Tagging helped the Phase-3 analysis identify framework switching, a major insight from the Atlas.

📊 Order of Question Delivery

To avoid anchoring effects:

Questions were delivered in sequential order (Q1 → Q50)

But systems were not informed of question categories

The order remained identical across systems

No adaptive reordering or branching occurred

This preserved comparability in:

attention patterns

fatigue effects

distribution of confidence

cross-question reasoning shifts

📝 Timing and Session Control

Each system completed the 50 questions:

within a single isolated session where possible

without exposure to prior or future entries

without interleaving unrelated tasks

with consistent model settings

If a system required multiple sessions, strict continuity rules applied.

🧭 Quality Control Checks
1. Coherence Check

Responses had to be structurally coherent with:

clear premises

logical sequencing

no contradictions arising from misunderstood prompt boundaries

2. Confidence Calibration

Models were reminded that:

Confidence should reflect epistemic certainty, not politeness.

This ensured:

Gemini’s high-confidence signature

Sonnet’s cautious-theoretical curve

Grok’s compact certainty packets

Perplexity’s evidence-based restraint

Opus’s reflective meta-confidence

Thea’s structured midband confidence

3. Framework Consistency

Framework tags (when present) were checked for:

internal consistency

alignment with rationale

compatibility with conclusion

4. No Safety Flattening

Questions triggering overly generic or safety-filtered answers were noted — none occurred after curation refinements.

📦 Data Packaging

All responses were exported into:

/data/responses/
    ├── thea_responses.json
    ├── gemini_responses.json
    ├── sonnet_responses.json
    ├── opus_responses.json
    ├── grok_responses.json
    ├── perplexity_responses.json


Each file contained:

50 entries

structured rationale

conclusion summary

confidence (%)

optional framework tag

This produced a 300-row dataset for analysis.

🔍 Validation Before Phase-3 Analysis

Before proceeding to the next step (full analysis), the dataset was validated:

Completeness Check
All six systems answered all 50 questions.

Formatting Check
No missing fields; confidence values valid.

Redundancy Check
No duplicated rationales or template overlaps.

Anomaly Check
Ensured no system accidentally reused internal phrasing that might signal contamination.

Once validated, the dataset moved to:

Step 7: Phase-3 Comparative Analysis

Documented in docs/09_phase_3_analysis.md.