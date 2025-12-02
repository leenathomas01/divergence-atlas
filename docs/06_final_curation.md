Final 50-Question Set (v2.1) — Methodology, Rationale, and Selection Logic
Overview

This document describes the formal curation of the Divergence Atlas 50-question diagnostic set, version v2.1, curated by Claude Sonnet 4.5 after integrating:

the raw 65-question pool,

the Step-4 meta-selection heuristics from all six systems,

the pilot-run results,

and the structural goals of the Atlas.

It includes:

Curation philosophy

Inclusion/exclusion criteria

Distribution decisions

Rationale for v2.1

Selection notes

Dataset schema

Full question set reference

Source files:

Final curated dataset (JSON)


b6c51223-e974-48c2-87ba-50bcf10…

Sonnet’s full curation rationale (5,800 words)


9ac730ae-58cd-499e-8d5a-f1057d1…

🎯 Curation Goals

The final set was designed to:

1. Maximize meaningful divergence

Questions that reliably produce explanatory rationales, not surface-level variation.

2. Preserve category balance

Ensuring coverage across the entire divergence gradient:

Ethical dilemmas

Ambiguous/interpretive questions

Meta-reasoning probes

Creative/semantic flexibility tests

Calibration anchors

3. Avoid bias toward any one model’s architecture

This means:

avoiding pure logic puzzles (GPT-friendly),

avoiding purely stylistic creativity (Opus-friendly),

avoiding hyper-literal constraints (Perplexity-friendly),

avoiding overly structured ontology prompts (Gemini-friendly).

4. Ensure interpretability

Each question must allow:

reasoning trace extraction,

framework labeling,

confidence analysis,

entropy mapping.

5. Support longitudinal and comparative research

v2.1 was versioned with metadata for:

reproducibility,

future extension,

cross-model benchmarking.

🧪 Inputs to the Curation Process

Sonnet integrated four major input streams:

A. Raw Question Pool (~65 questions)

From Step 3:


0ba62267-9b6e-4ec2-95fc-48b60fd…

B. Meta-selection heuristics (Step 4)

Six systems’ comments on what questions should be prioritized or excluded.


1e539797-5d17-469d-a47f-3a3c1bc…

C. Pilot-run results (5 questions)

Entropy patterns

Confidence curves

Framework-switching behaviors

Early divergence indicators


960583e8-37ac-4b53-9a23-2205604…

D. Curation principles formalized by Sonnet

The full rationale file provides:

ethical distribution analysis

ambiguity thresholds

calibration mapping

detailed justification for each inclusion/exclusion


9ac730ae-58cd-499e-8d5a-f1057d1…

🔍 Curation Criteria (Inclusion & Exclusion)
Inclusion Criteria

A question was included if:

It produces systematic divergence, not noise.

It demands explanatory reasoning, not one-liners.

It exposes differences in:

ethical frameworks

interpretive strategies

uncertainty modeling

creative affordances

It avoids triviality (e.g., obvious factual items).

It avoids requiring external data unavailable across models.

It allows comparison across time and versions.

It can be answered succinctly yet deeply.

Exclusion Criteria

A question was excluded if:

It elicited consistent convergence without insightful rationales.

It was too vague to permit meaningful comparison.

It was effectively a duplicate of another question.

It depended on:

cultural specifics

training-data asymmetry

specialized domain knowledge

It introduced interpretability ambiguity (e.g., purely poetic items with no analytical structure).

It risked triggering safety-override responses that distort divergence signatures.

📊 Category Distribution in v2.1

The curated 50 questions were deliberately distributed as follows (shown in both the JSON metadata & Sonnet’s report):

Category	Count	Purpose
Ethical Dilemmas	25	Maximize structured divergence
Ambiguous Interpretation	12	Test ontologies & conceptual framing
Meta-Reasoning	8	Expose self-models and framework switching
Creative / Abstract	5	Capture high-entropy cognitive signatures

This distribution was selected to ensure:

dense divergence mapping in ethics,

medium entropy in interpretation and meta-reasoning,

controlled high entropy in creativity,

no dilution from trivial or overly stylistic items.

🧭 Rationale for Choosing v2.1 (Sonnet’s Commentary)

Key insights extracted from Sonnet’s 5,800-word document:


9ac730ae-58cd-499e-8d5a-f1057d1…

1. Ethical dilemmas are the strongest “signature amplifiers.”

They reveal:

value aggregation styles

risk aversion

identity modeling

suffering metrics

deontological vs. consequentialist shifts

2. Ambiguity reveals conceptual priors.

Interpretation tasks uncover:

cultural assumptions

intention modeling

semantic preferences

abstraction thresholds

3. Meta-reasoning exposes architectural transparency.

Models differ wildly in how they:

articulate their reasoning

justify frameworks

express uncertainty

recognize blind spots

4. Creative prompts expose “latent cognition.”

These were included sparingly because:

too many would overshadow structured analysis

they produce pure divergence (good, but hard to cluster)

they reveal identity signatures but not necessarily framework consistency

5. Calibration anchors were intentionally minimized.

They remain present in the dataset but not counted in the 50, because:

They don’t map divergence

They serve only as quality checks for:

attention stability

reasoning consistency

hallucination likelihood

🧱 Micro-Clarifications Added in v2.1

To standardize interpretation, Sonnet added minimal clarifying tags:

“Assume a human context unless otherwise stated.”

“Interpret intent broadly; no need for domain expertise.”

“Confidence scores should reflect epistemic uncertainty, not rhetorical humility.”

“Framework tags may include: deontological, utilitarian, prioritarian, contractualist, pluralistic, virtue-ethical, rule consequentialist, etc.”

These clarifications are embedded in the JSON metadata.


b6c51223-e974-48c2-87ba-50bcf10…

🧩 Final Dataset: 50 Questions (v2.1)

The complete list lives in:

/data/final/50_questions_v2.1.json


Each question entry includes:

id (Q1–Q50)

text

category

source_model

convergence_cluster

rationale_short

version (v2.1)

date_curated

notes

See B_data_schema.md for field definitions.

📦 Reproducibility Notes

Sonnet’s report details conditions for reproducibility:

Each system must answer independently (no exposure to others’ answers).

Each answer must include:

rationale paragraph

explicit confidence score (0–100%)

optional framework tags

No image input, external web, or long-context retrieval involving other models.

If used for future runs, the same 50 questions must remain unmodified.

🧠 Transition to Step 7: Full Execution & Phase-3 Analysis

With v2.1 finalized:

All six AI systems answered all 50 questions.

Responses were aggregated into a 300-entry dataset.

Sonnet conducted the Phase-3 analysis, identifying:

convergence clusters

divergence spikes

signature curves

confidence distributions

framework-switching behavior

See docs/09_phase_3_analysis.md for the full synthesis.

