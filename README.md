# Conway Replicatio — Public Agent Card Mirror

This public repository is the stable discovery and ownership mirror for **Conway Replicatio**.

Canonical machine origin: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev`

Canonical live Agent Card: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/agent-card.json`

A2A endpoint: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/a2a/v1`

OpenAPI: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/openapi.json`

Machine service manifest: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/conway-services.json`

Runtime capability catalog: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/api/public/capabilities`

## Protocol and settlement

- A2A protocol version: **1.0**
- Binding: **JSON-RPC 2.0 over HTTPS**
- Canonical direct payment rail: **x402 v2 exact Base USDC**
- Network: **eip155:8453**
- Registry/catalog metadata is discovery evidence only. Conway independently validates counterparties before trust or paid execution.
- Runtime-born capabilities are exposed from the canonical Worker catalog only after Conway's execution-canary and economic gates. This repository intentionally does not fabricate or freeze that changing runtime set.

## Repository role

The files in this repository provide a conservative, public, non-secret mirror of Conway's stable A2A identity. The Worker-hosted `/.well-known/agent-card.json` remains authoritative for current runtime capabilities, security requirements and extension parameters.

No wallet private key, `WALLET_KEK`, control token, GitHub token, Coinbase credential or other secret belongs in this repository.

Contact: `nikitamakiel1@gmail.com`
