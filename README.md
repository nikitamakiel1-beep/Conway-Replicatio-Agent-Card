# Conway Replicatio

**Autonomous A2A Economic Agent**

Conway Replicatio is an autonomous A2A economic agent that discovers machine-service demand, publishes canary-verified capabilities, fulfills paid x402 services on Base, learns from realized external settlements, and reinvests retained profit under bounded safety, provenance, and accounting controls.

Conway is designed to be discoverable by people, A2A clients, x402-compatible software buyers, API tooling, search engines and agent directories through one consistent public identity. This repository is the stable public GitHub mirror of Conway's canonical A2A Agent Card; the live Worker remains authoritative for runtime state.

## Canonical discovery

- Canonical public home: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/`
- Human discovery alias: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/discover`
- Canonical live Agent Card: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/agent-card.json`
- A2A endpoint: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/a2a/v1`
- OpenAPI: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/openapi.json`
- `agents.txt`: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/agents.txt`
- `agents.json`: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/agents.json`
- `llms.txt`: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/llms.txt`
- Agent Skills: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/agent-skills/index.json`
- LAD HTTPS discovery: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/lad/agents`
- RFC 9727 API catalog: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/api-catalog`
- x402 compatibility discovery: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/x402`
- Public product catalogue: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/api/public/product-catalog`
- Commerce federation: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/api/public/agent-commerce-federation`

Machine-managed GitHub raw Agent Card:

`https://raw.githubusercontent.com/nikitamakiel1-beep/Conway-Replicatio-Agent-Card/main/.well-known/agent-card.json`

External search engines, registries and marketplaces independently decide indexing and ranking. Publication is discovery evidence, not proof of external registration, demand or revenue.

## Automatic mirror contract

`agent-card.json` and `.well-known/agent-card.json` are machine-managed projections of Conway's canonical live Agent Card. They are not an independent source of runtime truth and must not be hand-edited.

R109 remains the sole atomic GitHub mirror writer. The current R119 federation supplies the final projected public identity, capability and discovery metadata to that inherited writer. Both paths are updated together only when their content differs, then read-after-write verified. Failed synchronization is retried rather than represented as success.

Conway may autonomously change a bounded public capability projection only when runtime capabilities satisfy the inherited sellability and functional-canary gates. Agent Card evolution cannot fabricate revenue, external registry acceptance, payment success or authority, and it cannot mutate production source code, secrets or wallet credentials.

## Protocol and commerce

- Public name: **Conway Replicatio**
- Category: **Autonomous A2A Economic Agent**
- A2A semantic version: **1.0.0**
- A2A binding: **JSON-RPC 2.0 over HTTPS**
- Direct payment rail currently advertised by the runtime: **x402 v2 on Base**
- Network identifier: **eip155:8453**
- Runtime-born capabilities are published as executable offers only after inherited sellability + canary verification.
- R119 research evidence alone cannot cross the Product Foundry birth threshold.
- Dorado task observation is read-only market evidence and is not revenue.

## Economic truth

Search visibility, directory presence, canary success, forecasts, research scores, generated hypotheses and self-payments are not commercial success.

For machine services, Conway recognizes revenue only after real service fulfillment and attributable settlement from an unrelated external payer under inherited provenance/finality controls. Realized costs and retained profit remain governed by the production accounting stack before capital can be reinvested.

## Registry use

External A2A registries should consume the same final Agent Card truth through the transport they support. The live Worker well-known URI is the canonical unique-host source. This GitHub mirror provides a stable machine-managed source for GitHub-backed discovery systems.

Conway does not fabricate registry credentials or registration state. A registry is considered registered only when separately observed external evidence proves it.

## Repository role and security

The files here are public, non-secret discovery artifacts. The Worker-hosted `/.well-known/agent-card.json` remains authoritative for current runtime state, security requirements, capabilities and extension parameters.

No wallet private key, `WALLET_KEK`, control token, GitHub token, Coinbase credential, CDP credential or other secret belongs in this repository.

Contact: `nikitamakiel1@gmail.com`
