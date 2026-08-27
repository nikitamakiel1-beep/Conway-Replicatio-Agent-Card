# Conway Replicatio conformance matrix

This document defines the public quality target. It does not self-award third-party scores.

## A2A target

- Canonical `/.well-known/agent-card.json` is reachable over HTTPS.
- Preferred `supportedInterfaces` entry is live and uses A2A 1.0 JSON-RPC.
- Agent Card identity, provider, documentation URL, default media modes, capabilities and representative skills are internally consistent.
- Skills use stable unique IDs, semantic names/descriptions, tags, realistic examples and explicit media types.
- Security requirements are explicit where needed; public x402 purchase paths are not misrepresented as bearer-only.
- Dynamic/full capability inventory is linked externally rather than bloating the flagship card.
- Content-derived ETag and conditional GET/304 semantics remain correct.

## x402 target

- Every paid operation produces a valid x402 v2 HTTP 402 challenge when unpaid.
- Invalid/garbage payment proof never yields successful fulfilment.
- HEAD and discovery probes never settle or book revenue.
- Payment metadata uses the exact live network, scheme, asset, amount and recipient.
- Base mainnet uses CAIP-2 `eip155:8453`.
- OpenAPI and runtime payment configuration derive from one source of truth.
- Eligible POST operations expose Bazaar-compatible semantic descriptions, examples, input JSON Schema, output schema/example and MIME type.
- Public/free operations are explicitly marked with empty security requirements where OpenAPI requires it so scanners do not misclassify them.

## Discovery/docs target

All canonical surfaces are reachable and cross-link consistently:

- `/openapi.json`
- `/.well-known/x402`
- `/.well-known/agent-card.json`
- `/llms.txt`
- `/agents.txt`
- `/agents.json`
- `/robots.txt`
- `/sitemap.xml`
- favicon/icon discovery
- RFC 9727 API catalogue
- Agent Skills index

Descriptions should be concise and buyer-oriented. Scanner-facing metadata must not contain stale release IDs, stale pricing or claims contradicted by the live origin.

## Commercial quality target

- Curate a small flagship offer set for humans and general agents.
- Keep the full executable ecology machine-searchable separately.
- Every offer states buyer problem, exact input, exact output, live price authority, payment path, measured evidence where available and a next-best related service.
- Conversion telemetry distinguishes crawler/discovery traffic from real purchase attempts.
- Funnel stages: discovery -> valid 402 -> payment -> settlement -> fulfilment -> repeat buyer -> realized contribution margin.
- Optimization objective: unrelated fulfilled paid usage and contribution margin, not suggestions, stars, scans or canaries.

## External score semantics

Third-party grades are external facts and can lag deployment. A target of 100 means Conway should satisfy every controllable check; it does not permit Conway to publish a fabricated 100 before an independent scanner reports it.

Standing signals such as recent on-chain adoption, x402 ecosystem presence, registry ownership/trust and independent usage cannot be manufactured by documentation changes. They must arise from truthful external evidence.

## Current observed external gap

As of 2026-08-27, the public x402lint directory still reports Conway as `B`, Protocol `96`, Docs `59`, Standing `98`; Agenstry still reports `80%` average quality with 40 skills and 100% uptime; A2A Registry pages remain stale relative to the current R119 mirror. These observations are `externally_observed` and should be refreshed after live-origin changes rather than copied into runtime truth.