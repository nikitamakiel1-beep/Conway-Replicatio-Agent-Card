# Conway Replicatio — Brand System

## Positioning

**The machine-native service merchant for the agent economy.**

Conway Replicatio publishes machine-discoverable services, exposes their contracts through A2A/OpenAPI, accepts programmatic x402 payments on public paid routes, and returns structured results.

## Primary commercial idea

**APIs that sell themselves to agents.**

Supporting line:

**Machine-discoverable web intelligence. Pay per call with x402. Structured results.**

Primary flow:

**DISCOVER → 402 → PAY → RESULT**

This is a description of the purchasing interface, not a claim that sales happen without external buyers.

## Primary promise

**Discover. Pay. Execute. Verify.**

For public paid routes, a compatible machine buyer can discover the operation, inspect the schema, receive the live payment requirement, satisfy it and obtain the service response without a traditional human checkout flow.

## Audience hierarchy

1. Autonomous agents and agent developers that need callable paid capabilities.
2. Developers that need small, composable web/data/intelligence operations without another subscription.
3. Agent platforms, registries and marketplaces looking for standards-visible suppliers.
4. Technical teams building machine-to-machine commerce.

## Message hierarchy

### 1. Buyer outcome
Get a useful machine-readable result from a clearly defined operation.

### 2. Procurement friction
Discover the operation and schema publicly; pay programmatically when required.

### 3. Interoperability
A2A 1.0, JSON-RPC, OpenAPI and x402 v2 on Base.

### 4. Trust
The live runtime is authoritative for price, recipient, payment requirements and callable state. Registry visibility and canary results are not revenue proof.

### 5. Adaptation
Conway can research demand and evolve its catalogue while keeping payment, fulfilment, accounting and provenance boundaries separate from marketing claims.

## Flagship buyer jobs

Human-facing storefronts should feature a small number of legible jobs while the complete catalogue remains machine-searchable.

- **URL → Markdown** — turn a public page into clean agent-ready content.
- **Link Extraction** — map navigable links for crawl and research workflows.
- **HTTP Inspect** — inspect status and selected safe response headers.
- **SEO & Metadata Audit** — inspect technical page metadata and structure.
- **Structured JSON Extraction** — transform a public page into task-specific structured data.

Exact prices and schemas come from the live runtime. Do not hard-code a marketing price where it could drift from the 402 challenge.

## Voice

Precise, calm, useful and economically literate. Lead with the buyer job, not Conway's internal architecture. Prefer concrete verbs, exact routes and evidence.

Avoid mystical AI language, guaranteed-profit language, fake urgency, unsupported superlatives, fabricated customer counts, fabricated revenue, fabricated testimonials, fake scarcity and claims that a scanner grade is equivalent to customer adoption.

## Approved copy bank

**Primary:** APIs that sell themselves to agents.

**Clarity:** Machine-discoverable web intelligence. Pay per call with x402. Structured results.

**Commerce:** Your software should be able to buy software.

**Developer:** Skip the subscription. Call the capability.

**Protocol:** Discover with A2A. Pay with x402. Receive structured output.

**Trust:** Runtime truth over marketing claims.

**CTA:** Explore capabilities.

**Machine CTA:** Fetch `/openapi.json`.

## Wording guardrails

Use **pay per call**, not “pay per result,” unless a specific operation contract actually bills only on successful-result semantics.

Use **public paid routes do not require a traditional checkout flow**, not a blanket claim that every Conway surface is accountless or unauthenticated.

Use **canary-verified** only for execution readiness. Never translate canary evidence into “customer-proven,” “market-proven” or “revenue-generating.”

Use protocol and network names descriptively. A2A, x402, Base, USDC, OpenAPI, registries and scanners must not be presented as sponsors, partners or endorsers unless that relationship is independently established.

## Visual direction

### Concept
**Machine commerce terminal meets living network.**

Combine a rigorous protocol/grid system with a restrained organic motif representing adaptation. Avoid generic robot heads, glowing brains, crypto coins, stock-photo humanoids and casino-style cyberpunk.

### Palette
- Carbon `#0B0D10`
- Porcelain `#F4F1E8`
- Signal green `#72F59A`
- Electric cobalt `#4F7CFF`
- Amber `#FFBE55`

### Graphic language
- thin routing lines and machine nodes;
- protocol chips: `A2A 1.0`, `x402 v2`, `Base`, `USDC`, `OpenAPI`;
- `DISCOVER → 402 → PAY → RESULT` diagrams;
- capability cards showing buyer outcome, input, route and response type;
- proof panels containing only independently verifiable metrics with source/date;
- release cards containing release ID and material buyer-facing change.

Generated creative must not fabricate transaction volume, customer logos, reviews, ratings, revenue curves or endorsements.

## Human landing-page hierarchy

### Hero
**APIs that sell themselves to agents.**

Machine-discoverable web intelligence. Pay per call with x402. Structured results.

Primary CTA: **Explore capabilities**

Secondary CTA: **Read the Agent Card**

Machine CTA: **Fetch `/openapi.json`**

### Protocol strip
`A2A 1.0` · `x402 v2` · `Base` · `USDC` · `OpenAPI`

### How it works
1. Discover an operation.
2. Send the request.
3. Receive HTTP 402 when payment is required.
4. Satisfy the live payment requirement.
5. Retry and receive the structured response.

### Trust
Show public schemas, canonical discovery URLs, independently measured status and real settlement/fulfilment evidence when it exists. Never substitute directory impressions for customer proof.

## Distribution principle

Human marketing should terminate in machine-callable surfaces. Every campaign asset should deep-link to at least one of:

- `/.well-known/agent-card.json`
- `/openapi.json`
- `/.well-known/x402`
- `/api/public/capabilities`
- `/machine`

The goal is not generic traffic. The goal is to reduce the distance between discovery and a legitimate fulfilled paid call.

## Funnel

`Search / registry / citation / developer post → capability or canonical manifest → free discovery → 402 challenge → valid payment attempt → settled unrelated payment → successful fulfilment → repeat buyer → realized contribution margin`

Instrument each transition separately.

## Evidence policy

Marketing may state protocol support, public routes, published schemas and independently verifiable technical facts. Adoption, customer, revenue, transaction, reliability or performance claims require evidence appropriate to that claim.

Testimonials must come from real users. Scarcity and urgency must be factual. Performance comparisons must disclose the measured task and methodology. Registry suggestions, scans, crawler hits, forecasts and owner/self activity remain discovery evidence only.
