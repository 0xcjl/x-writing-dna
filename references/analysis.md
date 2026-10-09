# Evidence-backed profiles

## Annotate all accepted works

For each work record: URL, topic, genre/subtype, opening device, central claim, evidence source, progression/turn, ending device, distinctive language, quoted/prompt/code spans, campaign/coauthor tags and a counterexample to any emerging general rule. Use brief notes rather than repeating full bodies.

Add three concise fields to the annotation file, or a work-ID-linked supplement when preserving an existing file:

| Field | Record | Missing evidence |
| --- | --- | --- |
| `judgment_origin` | Who makes the claim; source type; a short anchor; whether evidence is self-reported or independently checked | `unclear` when the text does not establish the origin |
| `choices_tradeoffs` | Named options, chosen/rejected route, stated reason, constraint/cost and outcome status | `not_observed` when no choice is stated; do not supply a plausible reason |
| `evaluation_criteria` | The explicit or text-supported standard used to evaluate the subject; anchor and any failure condition | `not_observed` or `unclear`; a one-work pattern remains a candidate |

The audit's character/paragraph counts describe **raw captured text**, including any embedded material. For narration statistics, create a separate analysis body with traceable excluded spans. Never report whole-body statistics as author-narration statistics when prompt blocks dominate.

## Six axes, separated by genre

1. Language: sentences/paragraphs, address to reader, punctuation, modal/hedging words, humor, self-positioning. State counting method and language; Chinese character counts and English word counts are not interchangeable.
2. Structure: hook, evidence placement, turn, close, list/thread/article organization.
3. Topic selection: reader problem, timeliness, ordinary vs viral samples, thematic concentration.
4. Evidence: firsthand narrative, demonstrations, interviews, public research, numbers, screenshots. Author claims of testing are not independently reproduced tests.
5. Reasoning: recurring comparison axes, causal chains, conditions, counterarguments and uncertainty.
6. Visual role: screenshots as proof/instruction, diagrams, image-led pacing. Inspect representative visuals through the browser. Attribute platform fonts/layout to the platform unless author control is demonstrated.

## Three content-context dimensions, separated by genre

### 1. Judgment origin / 判断的来路

Distinguish an author's self-reported experience or observation, attributed public research/case, quotation, value preference and current hypothesis. Identify mixed origins where useful. Author-owned text does not prove a self-reported result. Embedded AI text, interviewees and quoted authors retain their own speakers.

Describe how the author connects origin to a conclusion: what prompted the judgment, which evidence changed it and how uncertainty is stated. When the connection is absent, report absence. Use source works and short anchors, not psychological speculation.

### 2. Choices and tradeoffs / 选择与取舍

Extract options actually mentioned, what was chosen/rejected, the stated reason, relevant constraints, accepted cost and reported outcome. Separate intended action, completed action and verified outcome. A strong opinion without alternatives is not automatically a documented tradeoff.

Look for how a choice is made legible to readers: comparisons, turning points, failed attempts, changed views or a bounded recommendation. Report how often these appear within the analyzed genre; absent cases and campaigns help limit the claim.

### 3. Recurring evaluation criteria / 稳定的评价标准

Identify the standards repeatedly used to judge tools, products, opportunities or claims, such as reproducibility, human effort, value rights or evidence quality. Require at least 3 independent works per analyzed genre before calling a standard recurring. Separate explicit standards from interpretive candidates. Include contrary cases and topic/campaign concentration.

Phrase the conclusion as an observed textual practice within the sample. A repeated criterion is not proof of lifelong values, private motives or a psychological personality. With fewer works, retain a scoped candidate rather than filling the section with a confident identity claim.

## Profile format

Start with scope and sample quality. Give one organizing principle for the observed style, followed by 3–5 reusable mechanisms. For each: what the author does → how it changes reading → 3+ work IDs → observed frequency and denominator → exceptions → a practical transfer rule. Keep minor quirks out of the core identity.

Include what should not transfer (unverified product/market/earnings claims, manufactured first-person scenes, repetitive CTA, trademark phrases). Distinguish textual style from inferred cognition and from distribution success. Popularity is associated evidence, never causal proof.

Include one section for each new content-context dimension in `post-dna.md` and `article-dna.md`. State the observed works/denominator, anchors, contrary or absent cases, interpretation strength and transferable expression action. Genuine absence is a result. Existing six-axis profiles are historical outputs until this supplement is read and added; do not relabel them as already analyzed under the new dimensions.

For a training handoff, attach a compact method entry: name, genre, organizing principle, 3+ source work IDs/URLs, applicable reader/material conditions, practice action, limitations and a sign of misuse. Transfer the expression method; keep author-specific life facts and beliefs out of the user's personal material cards.

## Same-author comparison

Compare the same author's short and long branches on hook, claim density, narrative/evidence order, confidence, reader address, pacing and ending. Never use one author's posts and another author's articles as evidence of within-author differences. A missing branch stays missing.

## Validation

Freeze rules before opening held-out works. Predict specific observable patterns, then record held-out hits/misses and update rules that fail. Do not use a profile to fabricate text and treat that fabricated text as validating evidence. Cross-topic validation and user acceptance remain separate from count and schema checks.
