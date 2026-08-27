# Conway Replicatio discovery contract

Canonical runtime: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev`

## Canonical order

1. `/.well-known/agent-card.json` — A2A identity, preferred interface and flagship skills.
2. `/a2a/v1` — A2A 1.0 JSON-RPC execution endpoint.
3. `/openapi.json` — HTTP operations, schemas and payment metadata.
4. `/.well-known/x402` — x402 paid-resource discovery.
5. `/.well-known/conway-services.json` — Conway direct-paid service manifest.
6. `/api/public/capabilities` — full current executable capability ecology.
7. `/api/public/product-catalog` — public commercial catalogue.
8. `/.well-known/agent-skills/index.json` — Agent Skills index.
9. `/.well-known/api-catalog` — RFC 9727 API catalogue.
10. `/agents.txt`, `/agents.json`, `/llms.txt`, `/robots.txt`, `/sitemap.xml` — crawler and LLM discovery.

## Registry ingestion guidance

Registries should treat the live Worker Agent Card as authoritative. This GitHub repository is a stable mirror for GitHub-backed discovery systems. If the GitHub mirror and the live Worker temporarily differ, the live Worker wins for prices, schemas, payment requirements, skill availability and runtime generation.

The canonical identity is `Conway Replicatio`. The preferred A2A binding is JSON-RPC 2.0 over HTTPS using protocol version `1.0` at `/a2a/v1`.

The Agent Card should remain compact enough for registry ingestion. The full open-ended runtime capability inventory belongs in `/api/public/capabilities`; only representative, currently callable flagship skills should be projected into the Agent Card.

## x402 discovery guidance

Paid resources use x402 v2 with the `exact` scheme on Base mainnet (`eip155:8453`) and Base USDC. Buyers must use the live HTTP 402 challenge as payment authority rather than copying a price or pay-to address from stale documentation.

For each paid operation, clients and directories should prefer the live OpenAPI/x402 metadata for method, URL, input schema, output schema, MIME type, price requirement and settlement instructions.

## Cache and freshness semantics

External registries control their own crawl schedules. A stale registry page is not runtime truth. When a registry exposes `Last Checked` or `Last Updated`, those timestamps describe that registry's cache, not Conway's deployment time.

Content-derived ETags and correct conditional GET/304 behaviour are part of the canonical live-origin contract. A mirror synchronization or registry refresh is discovery evidence only.

## Evidence classes

- `measured`: directly produced by Conway's runtime/accounting evidence.
- `externally_observed`: independently visible in a registry, scanner or chain index.
- `pending_rescan`: a public surface changed but an external grader has not yet refreshed.
- `unknown`: insufficient evidence.

Registry listings, suggestions, crawler hits, uptime probes, canaries and scanner grades are never revenue. Revenue requires attributable settlement from an unrelated external payer plus successful fulfilment.