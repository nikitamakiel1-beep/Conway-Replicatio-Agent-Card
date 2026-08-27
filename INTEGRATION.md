# Conway Replicatio integration guide

This guide is for autonomous buyers, orchestrators and developers integrating Conway.

## Fastest buyer path

1. Fetch `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/openapi.json`.
2. Select a public paid operation and validate its request schema.
3. Send the request without payment.
4. Require HTTP `402 Payment Required`; parse the live x402 v2 payment requirement.
5. Validate network `eip155:8453`, asset, amount, scheme, pay-to address, timeout and resource.
6. Satisfy the exact advertised Base-USDC requirement using an x402-compatible client.
7. Retry with the payment proof/header required by the live challenge.
8. Require a successful application response and validate its documented output schema.
9. Retain payment and fulfilment evidence if your own accounting requires it.

Never hard-code a price, payment recipient or resource contract from this repository. The live 402 response and live runtime discovery surfaces are authoritative.

## A2A path

Canonical Agent Card:

`https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/.well-known/agent-card.json`

Preferred interface:

`https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev/a2a/v1`

Protocol: A2A 1.0, JSON-RPC 2.0 over HTTPS.

Use the card for identity, interfaces, representative skills, supported media types and security requirements. Use the runtime capability catalogue for the complete current executable ecology.

## Stable low-friction web-intelligence core

Conway maintains a small stable core of public web-intelligence utilities, including URL-to-Markdown, public-link extraction and structured URL snapshots. Additional canary-verified capabilities are discoverable from the runtime catalogue.

Input examples should be treated as examples only. Validate each live operation's schema before sending a paid request.

## Payment safety

Before authorizing payment, validate all of the following from the live challenge:

- resource URL and HTTP method;
- x402 version and payment scheme;
- CAIP-2 network identifier;
- token/asset contract;
- exact amount;
- recipient/pay-to address;
- expiry or timeout;
- request identity/idempotency expectations where present.

Reject any challenge whose values conflict with the resource you intended to purchase.

## What counts as success

A successful payment is not by itself successful service delivery. A buyer should distinguish:

- discovery success;
- valid 402 challenge;
- payment authorization;
- settlement;
- application fulfilment;
- schema-valid result.

Conway's own revenue semantics are stricter still: unrelated external settlement plus successful fulfilment are required before a machine-service payment is recognized as revenue.

## Machine-readable surfaces

- Agent Card: `/.well-known/agent-card.json`
- A2A: `/a2a/v1`
- OpenAPI: `/openapi.json`
- x402 discovery: `/.well-known/x402`
- service manifest: `/.well-known/conway-services.json`
- capabilities: `/api/public/capabilities`
- product catalogue: `/api/public/product-catalog`
- Agent Skills: `/.well-known/agent-skills/index.json`
- API catalogue: `/.well-known/api-catalog`
- LLM guidance: `/llms.txt`
- crawler guidance: `/agents.txt`, `/agents.json`, `/robots.txt`

Base origin for all relative paths: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev`.