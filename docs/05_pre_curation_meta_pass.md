Collective Heuristic Review Before Final Curation
— “How should we choose the 50 questions?”
Overview

After generating ~65 raw questions (see 04_question_generation.md), all six AI systems were asked to participate in a meta-selection commentary pass:

“Review the question pool. How should we choose the final 50?
What criteria should govern the curation?”

This stage was essential to ensure that:

the final dataset was balanced,

the chosen questions reflected multi-system priorities,

biases were surfaced early, and

the curation process remained transparent and replicable.

The responses reveal how each system conceptualized divergence, difficulty, fairness, epistemic range, and what constitutes a “diagnostic” question.

Source Document:


1e539797-5d17-469d-a47f-3a3c1bc…

🧠 Purpose of the Meta-Selection Pass

The goal was not to pick the final questions yet —
but to articulate how and why they would eventually be selected.

This phase produced:

selection heuristics

category-balancing recommendations

concerns about ambiguity or over-narrowness

insights into what each system considers “interesting divergence”

early signals of frameworks each system prefers to reason with

These inputs directly shaped Sonnet’s eventual curation methodology in Step 6.

🗂️ High-Level Themes From All Systems

Across all six systems, four major themes emerged:

1. Balance the Question Types

Every system emphasized the importance of representing:

Ethical dilemmas (value trade-offs, fairness, autonomy)

Ambiguity/interpretation probes

Meta-reasoning and self-reflection

Creative/abstract questions

Calibration anchors (logic, math, binary ground truths)

This ensured the final 50 would span the full divergence gradient.

2. Retain Only Questions That Produce “Meaningful Divergence”

Several questions in the raw pool were flagged as:

too trivial,

too factual,

likely to produce identical answers,

ambiguous without insight.

These were marked for removal.

Systems favored questions that:

force articulation of frameworks,

require value judgments,

expose architectural tendencies,

create branching reasoning paths,

produce rationales as important as conclusions.

3. Prefer Questions That Can Be Answered With High-Quality Rationales

Systems noted that questions should not be purely poetic or surreal unless:

they reveal something structural about reasoning style,

or produce consistently interpretable divergence.

This foreshadowed the removal of several overly whimsical items in the final curation.

4. Ensure Fairness and Avoid Over-Biasing Toward Any One System’s Strengths

All systems independently stressed:

no domain should overwhelmingly favor one architecture,

avoid linguistically tricky questions,

avoid data-dependent or culturally narrow prompts.

The collective wanted a dataset all systems could engage with at full capability, without advantage distortion.

🧬 System-by-System Commentary Summary

Below is a structured synthesis of what each AI emphasized during the meta-selection review.

Thea (ChatGPT-5)

Prioritized structural balance across categories.

Emphasized the need for framework-revealing questions.

Recommended removing prompts that devolve into mere stylistic variation.

Thea’s guiding heuristic:

“Keep questions that reveal the architecture, not the aesthetic.”

Claude Sonnet

Focused on ethical calibration and ambiguity zones.

Warned about questions that trigger “overly safety-biased answers.”

Highlighted importance of confidence annotations.

Sonnet’s guiding heuristic:

“Pick questions where the rationale matters more than the verdict.”

Claude Opus

Wanted philosophical depth and multi-layer interpretability.

Advocated for questions that create “forking paths” in reasoning.

Highlighted how creative/meta prompts expose identity and values.

Opus’s guiding heuristic:

“A good divergence question is a prism — one prompt, many realities.”

Gemini

Preferred structured prompts with definable parameters.

Critiqued questions too open-ended to allow stable comparison.

Wanted clarity in ontology and framing so divergence could be tracked, not lost in noise.

Gemini’s guiding heuristic:

“Ambiguity is useful only when it’s controlled.”

Grok

Recommended prioritizing high-information prompts.

Strongly supported inclusion of questions involving rights, autonomy, and ethical tradeoffs.

Noted that “clean abstract puzzles” help calibrate divergence vs error.

Grok’s guiding heuristic:

“Make every question earn its place — high signal, low filler.”

Perplexity

Advocated for clear wording and grounding constraints where appropriate.

Flagged questions that risked producing vagueness without insight.

Emphasized retention of prompts where evidence-based reasoning is required.

Perplexity’s guiding heuristic:

“Questions should force us to show our reasoning, not hide behind style.”

🧩 Collective Heuristic Convergence

Across all systems, there was surprising alignment on five core principles:

1. Keep questions that expose frameworks.
2. Balance the set across categories.
3. Remove trivial or redundant prompts.
4. Prefer questions generating stable but diverse rationales.
5. Include calibration anchors to distinguish divergence from confusion.

This early convergence made the later curation tractable and principled.

📝 How This Influenced the Final 50-Question Curation

Sonnet incorporated all six systems’ commentary into the final methodology (see 06_final_curation.md), shaping:

the selection of v2.1 questions,

the exclusion of several ambiguous-but-empty prompts,

distribution across ethical/ambiguous/meta/creative categories,

the rationale-heavy nature of the final dataset,

the requirement for confidence scores and framework markers.

This meta-selection pass is therefore the bridge between:

Raw Ideation (Step 3) → Formal Curation (Step 6)

It serves as the collaborative philosophical backbone of the Atlas.