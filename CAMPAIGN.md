# Conway Replicatio — Campaign System

## Campaign idea

**Software that can buy software.**

Conway is positioned as a machine-native service merchant: discoverable by agents, callable over public interfaces, payable with x402 and accountable to runtime evidence.

Primary campaign line:

**Discover. Pay. Execute. Verify.**

Primary commercial headline:

**APIs that sell themselves to agents.**

## Buyer stories

### Agent developer
**Problem:** My agent needs a capability now, without another account or subscription.

**Promise:** Discover the operation, read the schema, satisfy the 402 and receive a structured result.

**CTA:** Fetch the OpenAPI document.

### Autonomous agent
**Problem:** I need a machine-readable supplier I can evaluate and purchase from programmatically.

**Promise:** Stable discovery, explicit schemas, x402 payment requirements and deterministic response contracts.

**CTA:** Fetch the Agent Card.

### Platform / marketplace
**Problem:** I need suppliers that are standards-visible, parseable and safe to index.

**Promise:** Canonical A2A, OpenAPI, x402, Agent Skills and crawler/LLM discovery surfaces that resolve to one identity.

**CTA:** Index the canonical origin.

## Flagship funnel

`DISCOVER → UNDERSTAND → 402 → VALIDATE → PAY → SETTLE → FULFIL → VERIFY → REPEAT`

Every public marketing surface should make the next step obvious.

## Message stack

1. **Outcome:** Get a useful machine-readable result.
2. **Friction:** No traditional checkout for public paid routes.
3. **Interoperability:** A2A 1.0, JSON-RPC, OpenAPI, x402 v2, Base USDC.
4. **Trust:** Runtime payment metadata is authoritative.
5. **Evidence:** Visibility and canaries are not revenue; unrelated settled-and-fulfilled usage is.
6. **Adaptation:** Catalogue evolution follows measured demand rather than self-generated hype.

## Creative families

### Hero
**APIs that sell themselves to agents.**
Machine-discoverable services. Programmatic payments. Structured results.

### Problem / solution
**Your agent found the API. Can it buy it?**
Conway gives software a direct path from discovery to paid execution.

### Commerce
**Your software should be able to buy software.**
Pay per useful call, not per seat.

### Protocol
**A2A discovers it. x402 pays for it. Conway fulfils it.**

### Trust
**Runtime truth over marketing claims.**
Schemas, prices and payment requirements come from the live origin.

### Developer
**Skip the subscription. Call the capability.**

## Distribution map

### Machine-first
- canonical A2A Agent Card;
- A2A registries;
- OpenAPI and x402-compatible indexing;
- `/.well-known/x402` compatibility discovery;
- Bazaar/facilitator discovery metadata;
- Agent Skills;
- `llms.txt` and `agents.txt`;
- API catalogues and machine directories.

### Human-assisted
- GitHub README and repository assets;
- capability demos;
- integration recipes;
- protocol explainers;
- release notes focused on buyer-facing change;
- developer communities where promotion is explicitly permitted;
- ecosystem launch posts linking directly to callable surfaces.

## Content programme

Each content cycle should publish one item from each category:

1. **Capability proof** — exact input, exact output, direct route.
2. **Integration** — minimal working client flow.
3. **Protocol education** — one A2A/x402 concept explained clearly.
4. **Quality evidence** — measured reliability or conformance with methodology.
5. **Commercial experiment** — what changed in offer/pricing and why.
6. **Discovery status** — registry/scanner propagation without presenting visibility as revenue.

## Conversion rules

Every capability promoted to humans should answer, above the fold:

- What job does this solve?
- What exact input is required?
- What exact output is returned?
- Where does the live price come from?
- How is payment completed?
- What evidence proves the route is callable?
- What should the buyer try next if the result is useful?

Do not feature a capability solely because it exists. Feature it because the buyer job is legible, the output is easy to evaluate and the route is currently executable.

## Pricing communication

Use **pay per call** and **live price from the runtime** as the default language.

Do not use:
- fake strike-through prices;
- fictitious scarcity;
- arbitrary “enterprise” anchoring without a real offer;
- claims that a higher price means higher quality absent evidence.

## Trust architecture

Marketing is allowed to state:
- protocol support that is live and verifiable;
- public routes and discovery surfaces;
- measured technical results with methodology;
- independently observed directory/scanner state with timestamp/source.

Marketing is not allowed to invent:
- customers;
- testimonials;
- revenue;
- settlement volume;
- external adoption;
- rankings;
- uptime history;
- performance comparisons;
- endorsements.

## Launch sequence

### 1. Foundation
Canonical identity, brand, flagship copy, machine manifests, examples, evidence policy.

### 2. Discovery refresh
Re-crawl registries and scanners after live-origin changes and verify that they consume the current identity.

### 3. Acquisition
Publish useful demos and integrations that terminate in exact machine endpoints rather than a generic homepage.

### 4. Purchase optimization
Measure the largest drop-off between discovery, 402, payment and fulfilment.

### 5. Retention
Detect repeated jobs and create higher-value compound offers from frequently chained primitives.

### 6. Reputation
Publish only privacy-preserving, evidence-backed usage and reliability proof once unrelated paid usage exists.

## North-star

**Fulfilled paid calls from unrelated external buyers with positive realized contribution margin.**

Everything else is diagnostic or supporting evidence.