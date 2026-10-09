# Collection and corpus contract

## Browser operation

Use the user's specified surface when available; otherwise disclose the connected browser and verify the logged-in account without changing it. Work in separate research tabs. Read a fresh page state after navigation, then extract rendered public DOM through the documented browser tool. Do not replace browser control with shell HTTP against authenticated X.

Discover links from the author's profile, Articles tab, visible search results or dated searches. Use latest and older windows, high-engagement and ordinary works, and multiple topics when available. Record the sampling method and gaps; do not equate the algorithm's first screen with the author's full style.

On X, identify the **primary author block and primary permalink**. Quoted cards may contain other usernames, dates, texts and article covers. Extract only primary authored text. A quoted article cover does not make a normal post an article. Expand Show more or open the detail. Article acceptance needs the full title and body through the ending. Store linked external articles separately from native X Articles. Keep a long post a post; keep a numbered multi-post thread a single thread.

For an external archive, require a visible X-to-archive link, archive-to-X link, or a verified exact-body match with a primary X work. Matching nickname/bio alone is provisional. If identity is pending, retain the body with `identity_status: pending`; analyze only the named archive with that limitation, without calling it confirmed X-author DNA.

Record each body's local hash and source URL. Use a connector's export or another explicitly supported export path. If the browser tool only returns text, persist the returned public body with file tools. An export may parse narrowly identified public-content tool-output blocks from this run's own log, but never copy the full chat, credentials or unrelated records.

## JSONL record

One object per work; a grouped thread contains its ordered parts and one concatenated body.

```json
{
  "author": "example",
  "medium": "post",
  "format": "short_post",
  "source_kind": "x_native",
  "url": "https://x.com/example/status/123",
  "title": "",
  "date": "2026-10-01T12:00:00Z",
  "date_source": "primary_permalink_time",
  "captured_at": "2026-10-08T12:00:00Z",
  "body": "Complete primary authored text",
  "author_verified": true,
  "identity_status": "confirmed",
  "identity_evidence": "Primary account label and permalink match example",
  "complete": true,
  "completeness_evidence": "Opened detail; no Show more; captured through ending",
  "group_id": "123",
  "coauthors": [],
  "exclude_reason": "",
  "campaign": "",
  "images": [],
  "metrics": null
}
```

`medium`: post, article, thread. `format`: short_post, long_post, x_article, external_article, thread. `source_kind`: x_native, author_archive, mirror. Explicitly label absent dates or metrics as null. Identity confirmation is an observation with evidence, not the helper's inference. `coauthors` lists additional writers, not quoted interviewees. Mirrors stay a separate source stratum even after authorship is corroborated.

`complete` applies to visible textual completeness. Image/video content has its own inspection status. Embedded images count and URLs do not establish that the visual evidence was understood. A paywall/ending not reached must set complete false.

## Checkpoint

Keep raw capture immutable after each completed batch. Normalization and exclusions go into a new JSONL file. `run-status.md` starts with stage, result, next action, then per-author/per-genre raw and confirmed counts, source classes, failure observations and remaining URLs. Resume by canonical URL and body hash, not by an assumed scrolling position.
