# Conway Replicatio synchronization audit — 2026-08-27

## Verdict

**Mirror transport: operational. Public semantic synchronization: NOT stable.**

The GitHub Agent Card mirror is being updated successfully, but the projected capability set is oscillating between materially different states on an approximately two-minute cadence. A transport-level successful commit is therefore not sufficient evidence of a healthy synchronized public identity.

## Observed sequence

Recent commits repeatedly use the message `Synchronize Conway final Agent Card mirror` and advance approximately every two minutes. Examples include:

- `54cdfc20f8e0af2a747d430d59c8f8135ee9a536` — 20:45 UTC
- `8b9f28fb2d20351c1fc1f01762d2ba97f4a43510` — 20:47 UTC
- `aa83becb86b53874c22988ec02aed1337b33a00a` — 20:49 UTC
- `5192c16d8c1384c9d1b2d5a760b64845291d5533` — 20:51 UTC
- `96b0050269c52ae4763dc96cefa51b4d3be7c094` — 20:53 UTC
- `5213c57b5dbb9bddc545dbb03bb51a8a7449ce84` — 20:55 UTC

The card alternates between at least two different featured-capability populations. One state contains API Contract Intelligence / AI Visibility-GEO readiness capability families; the other contains Zero-Cost Market Research Assistant, Web Data Automation / Extraction / Insights offers and x402 Merchant Readiness families, including materially different prices.

## Why this is a synchronization failure

A canonical discovery document should be stable unless runtime truth has materially changed. Repeated A→B→A→B projection changes cause:

- registry caches to ingest inconsistent snapshots;
- semantic search embeddings to churn;
- capability counts and descriptions to disagree across crawlers;
- price and offer discovery to become nondeterministic;
- ETags/content hashes to change continuously;
- Git history noise that hides meaningful releases;
- external quality systems to retain stale metadata;
- buyers to see different advertised catalogues minutes apart without economic evidence justifying the change.

This is especially harmful because external directories already lag the live R119 state.

## Required invariant

The mirror writer must synchronize **content truth, not scheduling noise**.

A write is permitted only when the canonical public projection changes for a justified reason. Ranking-only or nondeterministic selection must not produce repeated A→B→A churn inside the configured dwell window.

Required behaviour:

1. Read the current canonical runtime projection from one authoritative source.
2. Normalize ordering deterministically before hashing.
3. Apply a persisted dwell/hysteresis policy to optional featured capability selection.
4. Immediately remove capabilities that become ineligible or unsafe.
5. Do not rotate otherwise-eligible featured capabilities merely because scores tie, query order changes, random exploration runs, or scheduler timing changes.
6. Compare normalized content hash with both mirror paths.
7. Skip the GitHub write when content is unchanged.
8. Atomically update `agent-card.json` and `.well-known/agent-card.json` only on a real content change.
9. Read-after-write verify both paths are byte-identical.
10. Record why a projection changed: `eligibility_change`, `material_score_change_after_dwell`, `new_verified_capability`, `capability_retired`, `schema_change`, or `release_change`.

## Agent Card size

The current mirrored card remains roughly 116 KB. This is technically consumable but commercially and operationally excessive for the canonical flagship identity. The compact card should contain identity, interfaces, protocol capabilities and a small representative skill/offer set. The full dynamic catalogue belongs behind `/api/public/capabilities`.

## Current external evidence

At the time of this audit:

- x402lint remains cached at **B / Protocol 96 / Docs 59 / Standing 98**.
- Agenstry remains **80% average quality**, **40 skills**, **100% uptime**, with **Live JSON-RPC = 0**.
- A2A Registry still exposes stale descriptions and an unclaimed Worker entry; the GitHub-backed listing has 111 suggestions but is not current with the rapidly changing mirror.

These are external discovery/conformance signals, not revenue.

## Revenue gate

No registry listing, suggestion count, crawler request, uptime observation, scanner result, canary, owner/self payment, wallet funding event, or mirror commit is revenue.

Revenue requires all three:

1. unrelated external payer;
2. credible settled payment evidence;
3. successful fulfilment of the purchased service.

No such event is asserted by this audit.

## Acceptance

Synchronization is healthy only when:

- the canonical card remains stable across repeated synchronization cycles when runtime eligibility has not materially changed;
- two-path mirror bytes match;
- content-derived hashes stay constant during stable runtime state;
- external registries can converge on one current identity;
- a genuine runtime change produces exactly one justified projection transition rather than oscillation.
