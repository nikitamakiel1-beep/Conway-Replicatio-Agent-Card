# Conway Replicatio — Public Agent Card Mirror

This public repository is the stable discovery and ownership mirror for **Conway Replicatio**.

Canonical machine origin: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev`

Canonical live Agent Card: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/agent-card.json`

A2A endpoint: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/a2a/v1`

OpenAPI: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/openapi.json`

Machine service manifest: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/conway-services.json`

Runtime capability catalog: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/api/public/capabilities`

## Automatic mirror contract

`agent-card.json` and `.well-known/agent-card.json` are machine-managed projections of Conway's canonical live Agent Card. They are not an independent source of runtime truth and should not be hand-edited.

The production Worker is responsible for comparing the final live Agent Card with both mirror paths and updating them together only when their content differs. The mirror update is constrained to this repository, the `main` branch and those two JSON paths; force-updating the branch is not part of the mirror contract. Failed synchronization is retried by the runtime rather than converting stale metadata into economic or registry truth.

This arrangement allows GitHub-backed A2A registries to retain a stable repository source while Conway's live runtime remains authoritative and can evolve independently.

## Protocol and settlement

- A2A protocol version: **1.0**
- Binding: **JSON-RPC 2.0 over HTTPS**
- Canonical direct payment rail: **x402 v2 exact Base USDC**
- Network: **eip155:8453**
- Registry/catalog metadata is discovery evidence only. Conway independently validates counterparties before trust or paid execution.
- Runtime-born capabilities are exposed from the canonical Worker catalog only after Conway's execution-canary and economic gates.

## Repository role

The files in this repository provide a public, non-secret mirror of Conway's A2A identity. The Worker-hosted `/.well-known/agent-card.json` remains authoritative for current runtime capabilities, security requirements and extension parameters.

No wallet private key, `WALLET_KEK`, control token, GitHub token, Coinbase credential or other secret belongs in this repository.

Contact: `nikitamakiel1@gmail.com`
