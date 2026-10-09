---
name: x-writing-dna
description: Research an X author's writing style from complete public works, collecting and auditing posts and articles separately before producing evidence-backed style profiles. Use for X参考账号研究、作者文风提炼、帖子与长文风格分别分析、50帖或20篇语料研究.
---

# X Writing DNA

Turn an account URL into a traceable corpus and separate profiles for posts and long-form writing. This is an agent-operated browser workflow with a local audit helper, not a standalone crawler or a guarantee that X will expose every work.

## Scope and collection

Honor the requested accounts and genres. Default acceptance targets are **50 independent complete posts OR 20 independent complete articles per author**. If both genres are requested, each needs its own target. Never substitute another genre to pass a missing branch.

Before collecting, read [references/collection.md](references/collection.md). Use the available authenticated browser or an authorized official API. Inspect current browser documentation. Collect public author content only; do not extract cookies, private messages, hidden application state, or bypass access controls.

Save each complete record immediately to `capture.jsonl`; checkpoint after at most 5 works. Store URL, authorship evidence, date provenance, genre, complete body, source class and completeness evidence. A title, timeline preview, search snippet, or mirror's generated summary is a discovery lead, not a complete work. Preserve raw records; correct metadata in a separate normalized file.

Group a thread as one work. Exclude reposts, other people's quoted bodies, link-only supplements, literal duplicates, unfinished template placeholders and truncated bodies from acceptance counts. Separate coauthored works and repeated promotional campaigns. External archives require an identity link to the X author before entering that author's confirmed corpus.

Run the audit helper after normalization:

```bash
python3 scripts/corpus_audit.py /absolute/path/corpus.jsonl --author handle --out /absolute/path/audit
```

It writes `audit.json` and `sample-index.csv`, with raw, eligible-body, identity-confirmed and X-native counts kept distinct. It trusts explicit identity/completeness observations; it cannot establish them from a URL or character count. Read the rejection list before reporting a passed target.

When access fails, save the last successful sample, remaining URLs, visible failure, attempt history and next action. After 3 consecutive failed page loads, stop that branch and try one legitimate alternative source. Do not infer rate limiting without a visible signal. Continue an independent accessible branch. Report missing targets as partial; do not silently change the target or call a stalled run complete.

## Style extraction

Read [references/analysis.md](references/analysis.md) after collection. Read every accepted body; statistics supplement close reading. Record one concise annotation per work. Analyze posts and articles independently, with subtypes where the evidence supports them. Separate author narration from embedded prompts, code, interview quotes and AI-generated excerpts.

Alongside the six expression axes, annotate **judgment origin (判断的来路)**, **choices and tradeoffs (选择与取舍)** and **recurring evaluation criteria (稳定的评价标准)**. Distinguish what an author publicly says from independently verified experience. Record absent or unclear evidence without inventing motives. Report these three dimensions separately in each genre profile, with source works, denominators and exceptions; older profiles need a labeled supplement before claiming this coverage.

Produce:

- `post-dna.md` and/or `article-dna.md`: 3–5 distinctive mechanisms, each supported by at least 3 source works, denominators, variation and counterexamples.
- `genre-comparison.md` only when both branches have real evidence; otherwise state the missing comparison.
- `run-status.md`: actual counts, source/identity status, time windows, campaign/topic concentration, excluded samples, access blockers and confidence limits.

Numbered thresholds do not establish representativeness. A short campaign-heavy window supports a scoped profile, not a timeless personality diagnosis. Views/likes are dated observations and do not prove that style caused reach.

For validation, reserve 5 unseen independent works per analyzed genre before forming the profile. Freeze the profile, annotate the held-out works, and record which predictions held or failed. If all samples were already read, label holdout validation unperformed; do not invent a retrospective blind test. A drafting imitation test is separate and only runs when requested.

## Applying findings

Distill reusable mechanisms, not signature slogans, biographical claims, unverified earnings or another author's identity. Keep the user's editorial positioning and existing P/L definitions. If asked to design a personal voice, offer 2–3 coherent choices per genre, each with one dominant organizing principle and a clear evidence fit. Do not manufacture first-person experience to fit a style.

When handing off to `personal-content-dna` or another writer, provide the mechanism, genre, 3+ supporting work IDs, scope/limitations and a practice action. Keep the reference author's experiences and beliefs attributed to that author. A suggested method is a trial for the user; only actual user feedback establishes adoption.

## Attribution

Adapted from the six-axis analysis idea in [larashero3-dotcom/writing-dna-skill](https://github.com/larashero3-dotcom/writing-dna-skill), commit `ee3d97ee27268004b5187d97711161f44fc4aae4`. Collection, provenance, genre gates and audit code are added for this workflow. Upstream license is preserved in `LICENSE`.
