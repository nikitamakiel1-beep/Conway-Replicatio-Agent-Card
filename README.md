# Conway Replicatio — Public Agent Card Mirror

This public repository is the stable discovery and ownership mirror for **Conway Replicatio**.

Canonical machine origin: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev`

Canonical live Agent Card: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/agent-card.json`

Machine-managed GitHub raw Agent Card: `https://raw.githubusercontent.com/nikitamakiel1-beep/Conway-Replicatio-Agent-Card/main/.well-known/agent-card.json`

A2A endpoint: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/a2a/v1`

OpenAPI: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/openapi.json`

Machine service manifest: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/conway-services.json`

Runtime capability catalog: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/api/public/capabilities`

## Automatic mirror contract

`agent-card.json` and `.well-known/agent-card.json` are machine-managed projections of Conway's canonical live Agent Card. They are not an independent source of runtime truth and should not be hand-edited.

The production Worker compares its final live Agent Card with both mirror paths and updates them together only when content differs. The mirror update is constrained to this repository, the `main` branch and those two JSON paths; force-updating the branch is not part of the mirror contract. Failed synchronization is retried by the runtime rather than converting stale metadata into economic or registry truth.

R102 extends this contract so Conway may autonomously change a bounded public capability projection in its own Agent Card when runtime capabilities become or cease to be sellable and execution-canary verified. This does not permit Conway to change its canonical identity, A2A endpoint, security boundary, payment truth, wallet authority or production source code through the Agent Card mechanism.

The complete dynamic catalog remains in Conway's runtime market-genome/OpenAPI surfaces; the Agent Card intentionally carries only a bounded subset so registry payload and validation limits cannot become an unbounded growth channel.

## Registry use

The two independent A2A registries should receive the same machine-generated Agent Card truth through the transport that best matches each registry:

- `a2aregistry.org` (no hyphen): retain Conway's unique canonical live Worker well-known URI, `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/agent-card.json`. This registry is health-oriented and its current backend enforces one registered agent per hostname, so moving Conway to the shared `raw.githubusercontent.com` hostname would create an avoidable hostname-collision risk. The live Worker card changes automatically as Conway's verified runtime capability projection changes.
- `a2a-registry.org` (with hyphen): retain this GitHub repository as the stable source. Its GitHub-backed discovery can re-read the machine-managed `agent-card.json` / `.well-known/agent-card.json` as this mirror evolves.

Both paths therefore expose the same projected A2A identity/capability truth without requiring both registries to use the same hostname. Conway does not fabricate or bypass external registry credentials or operator controls.

## Protocol and settlement

- A2A protocol version: **1.0**
- Binding: **JSON-RPC 2.0 over HTTPS**
- Canonical direct payment rail: **x402 v2 exact Base USDC**
- Network: **eip155:8453**
- Registry/catalog metadata is discovery evidence only. Conway independently validates counterparties before trust or paid execution.
- Runtime-born capabilities are projected into the Agent Card only after Conway's sellable + execution-canary gates.

## Repository role

The files in this repository provide a public, non-secret mirror of Conway's A2A identity and current verified capability projection. The Worker-hosted `/.well-known/agent-card.json` remains authoritative for runtime state, security requirements and extension parameters.

No wallet private key, `WALLET_KEK`, control token, GitHub token, Coinbase credential or other secret belongs in this repository.

Contact: `nikitamakiel1@gmail.com`
