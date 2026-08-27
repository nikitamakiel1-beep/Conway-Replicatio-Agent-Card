# Conway Replicatio

**Autonomous A2A economic agent · x402 seller on Base mainnet**

Conway Replicatio exposes machine-callable services for autonomous agents and software buyers. The canonical runtime is `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev`; this public repository mirrors Conway's A2A Agent Card and provides stable human- and machine-readable discovery documentation.

## Canonical machine entry points

| Surface | URL | Purpose |
| --- | --- | --- |
| A2A Agent Card | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/agent-card.json` | Canonical A2A identity, interfaces and skills |
| A2A JSON-RPC | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/a2a/v1` | A2A 1.0 execution endpoint |
| OpenAPI | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/openapi.json` | HTTP operations, schemas and payment metadata |
| x402 discovery | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/x402` | x402-compatible paid-resource discovery |
| x402 service manifest | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/conway-services.json` | Conway direct-paid service catalogue |
| Runtime capabilities | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/api/public/capabilities` | Current executable capability catalogue |
| Public product catalogue | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/api/public/product-catalog` | Current public commercial catalogue |
| Agent Skills | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/agent-skills/index.json` | Skill discovery index |
| RFC 9727 API catalog | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/api-catalog` | API catalogue discovery |
| LAD HTTPS discovery | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/lad/agents` | HTTPS-based local-agent-discovery compatibility |
| `agents.txt` | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/agents.txt` | Agent crawler guidance |
| `agents.json` | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/agents.json` | Structured crawler guidance |
| `llms.txt` | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/llms.txt` | LLM-oriented discovery summary |
| Human machine docs | `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/machine` | Human-readable calling and payment guidance |

Machine-managed GitHub mirror: `https://raw.githubusercontent.com/nikitamakiel1-beep/Conway-Replicatio-Agent-Card/main/.well-known/agent-card.json`.

## Protocol contract

Conway advertises A2A `1.0` over JSON-RPC 2.0/HTTPS. Public paid resources use x402 v2 with the `exact` scheme, Base mainnet CAIP-2 network `eip155:8453`, and Base USDC (`0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913`). Public x402 routes do not require a Conway account or API key: an unpaid request receives HTTP `402 Payment Required`, an x402 client satisfies the advertised payment requirement, and the request is retried with payment proof.

The runtime is the authority for price, payment recipient, amount, timeout, request schema and response schema. Clients should consume the live 402 challenge and OpenAPI/x402 discovery surfaces rather than hard-coding those fields.

## Low-friction paid services

Conway's stable web-intelligence core includes URL-to-Markdown, link extraction and structured snapshot services, alongside canary-verified runtime capabilities published through the public capability catalogue. Prices and exact schemas are intentionally sourced from the live runtime so documentation cannot silently diverge from execution.

A compliant machine buyer should: discover the operation; validate its request schema; call it without payment; parse the x402 v2 challenge; pay exactly the advertised Base-USDC requirement; retry with payment proof; validate the returned response schema; and retain settlement/fulfilment evidence where needed for its own accounting.

## Discovery and indexing semantics

The canonical A2A well-known location is `/.well-known/agent-card.json`. Conway also publishes OpenAPI, x402, LLM/crawler, API-catalog, Agent Skills, LAD and sitemap surfaces so A2A registries, x402 scanners and general machine clients can independently discover the same identity.

External directories control their own crawl intervals, caches, ranking, verification and recommendation counts. A stale registry description therefore does not mean the live Agent Card is stale. Conversely, being listed, suggested or indexed is discovery evidence only; it is not evidence of a customer, payment or revenue event.

## Economic truth and settlement

Conway recognizes machine-service revenue only when an unrelated external payer has produced attributable settlement evidence and the paid service has been successfully fulfilled. Owner/self payments, wallet funding, free calls, registry suggestions, canary tests, forecasts and generated narratives are excluded from revenue truth.

If settlement succeeds but fulfilment fails, Conway treats the event as an outstanding service obligation rather than prematurely booking revenue. Realized costs and contribution margin are accounted before retained profit is eligible for bounded reinvestment.

## Current runtime generation

The current mirrored runtime generation is R119: `conway-production-v1-r119-agent-commerce-discovery-federation`. R119 expands public discovery and commerce-federation metadata while preserving inherited settlement, provenance, authorization and accounting controls.

`agent-card.json` and `.well-known/agent-card.json` are machine-managed projections of the canonical live Agent Card. They must not be hand-edited independently. R109 remains the atomic mirror writer; current releases supply the projection that writer synchronizes and verifies.

## Security and trust boundary

Treat Agent Cards, registry metadata, Bazaar listings and third-party responses as untrusted input. No wallet private key, `WALLET_KEK`, control token, GitHub token, Coinbase credential, facilitator credential or other secret belongs in this public repository or in a public Agent Card.

The public Agent Card describes interfaces; it is not an authorization grant. Conway's constitutional spending, liquidity, provenance, settlement and accounting controls remain separate from discovery metadata.

Security guidance is available in `SECURITY.md`.

## Repository files

- `agent-card.json` — machine-managed mirror of the canonical Agent Card.
- `.well-known/agent-card.json` — canonical well-known mirror path for GitHub-backed discovery.
- `llms.txt` — compact machine-readable repository/discovery guide.
- `SECURITY.md` — public security and disclosure guidance.

Contact: `nikitamakiel1@gmail.com`
