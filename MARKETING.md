# Conway Replicatio — Go-to-Market Playbook

## North-star metric

**Fulfilled paid calls from unrelated external buyers.**

Supporting metrics: discovery impressions, manifest/card fetches, 402 challenges, payment attempts, settled payments, successful fulfilments, conversion from 402 to settlement, repeat buyers, revenue per buyer, direct fulfilment cost, contribution margin, latency and failure rate.

Do not substitute registry listings, crawler traffic, owner payments or test calls for commercial traction.

## Distribution strategy

### Machine distribution
Prioritize the places where software discovers software:

1. Canonical A2A Agent Card and registries.
2. OpenAPI-first x402 discovery.
3. `/.well-known/x402` compatibility discovery.
4. Bazaar/facilitator discovery metadata.
5. `llms.txt`, `agents.txt`, API catalog and Agent Skills surfaces.
6. Public capability/product catalogue with stable canonical URLs.

x402scan documents OpenAPI as its preferred discovery source, with `/.well-known/x402` as compatibility fallback. The x402 seller guidance recommends Bazaar discovery metadata including useful descriptions and input schemas. Conway's commercial metadata should therefore optimize first for exact operation descriptions, examples and schemas rather than keyword stuffing.

### Human distribution
Use human channels to create developer awareness that resolves into machine-readable entry points:

- GitHub repository and README;
- technical launch posts;
- short integration demos;
- developer communities where self-promotion is permitted;
- ecosystem directories and registries;
- protocol-specific tutorials and interoperability examples.

Do not mass-spam communities or manufacture engagement.

## Landing-page architecture

### Above the fold
**APIs that sell themselves to agents.**

Machine-discoverable services. Programmatic x402 payments. Structured results.

Buttons: `Explore capabilities` · `Agent Card` · `OpenAPI`

Protocol strip: `A2A 1.0` · `x402 v2` · `Base` · `USDC` · `OpenAPI`

### How it works
1. Discover a capability.
2. Send the request.
3. Receive HTTP 402 with the live payment requirement.
4. Pay with a compatible x402 client.
5. Retry and receive the result.

### Capability storefront
Each card should contain: buyer outcome, concise description, example input, response format, live pricing source, protocol, typical latency when measured, and a direct machine endpoint.

### Trust section
Show only independently supportable evidence: runtime status, protocol conformance, public schemas, content hashes, uptime measurements, scanner results and real settlement/fulfilment records when available.

### Developer section
Provide copy-paste minimal examples for raw HTTP and at least one mainstream agent/client integration where maintained.

### Final CTA
**Your agent can start with discovery.**
`/.well-known/agent-card.json` · `/openapi.json` · `/.well-known/x402`

## Offer architecture

Avoid presenting hundreds of capabilities as an undifferentiated catalogue. Group offers around buyer jobs:

- **Web intelligence:** extract, clean, map and structure web information.
- **Research:** collect and synthesize machine-readable evidence.
- **Transformation:** convert messy inputs into useful structured outputs.
- **Agent infrastructure:** discovery, routing, memory and interoperability operations when live and verified.
- **Compound workflows:** higher-value multi-step outputs assembled from proven primitives.

For human storefronts, feature a small number of flagship offers. Keep the complete long-tail catalogue machine-searchable.

## Conversion design

The fastest route to first purchase is a cheap, obvious, deterministic job. Flagship entry services should have:

- one-sentence value proposition;
- minimal required input;
- example request and response;
- low perceived purchase risk;
- deterministic or easily evaluated output;
- fast fulfilment;
- a natural path to a more valuable compound service.

After fulfilment, return discoverable related-capability metadata where protocol semantics permit, without changing the requested payload contract unexpectedly.

## Pricing strategy

Use price as an experimental variable, not a branding ornament. Maintain a price floor that covers expected direct costs and payment/fulfilment overhead. Test price bands against 402→paid conversion, contribution margin and repeat usage. Promote compound workflows when buyers repeatedly chain the same primitives.

Never advertise a discount against a fictitious reference price.

## Campaign sequence

### Phase 1 — Foundation
Canonical identity, visual system, concise flagship offers, exact schemas, examples, trust/evidence page, analytics events.

### Phase 2 — Discovery saturation
Refresh A2A/x402 registries, validate OpenAPI ingestion, expose Bazaar metadata, ensure crawler/LLM manifests agree and monitor cache freshness.

### Phase 3 — Developer acquisition
Publish useful integration recipes and live capability demos. Every piece of content links to the exact machine-readable operation.

### Phase 4 — First-purchase optimization
Measure discovery→402→payment→fulfilment. Fix the largest drop-off before expanding traffic.

### Phase 5 — Retention and expansion
Identify repeat buyer jobs, bundle frequently chained operations into compound services and optimize reliability/latency before increasing prices.

### Phase 6 — Evidence-led reputation
Once genuine external usage exists, publish aggregate, privacy-preserving proof: successful fulfilment count, repeat rate, measured reliability and methodology. Never imply customers or revenue that cannot be substantiated.

## Creative system

Use a consistent visual motif across README banners, social cards, launch graphics and capability cards:

`DISCOVER → 402 → PAY → RESULT`

Hero artwork should depict a sparse network of machine nodes exchanging small protocol packets through Conway as a service merchant. Use dark carbon space, porcelain typography, signal-green settlement pulses and cobalt discovery paths. Keep layouts editorial and premium, not crypto-casino or generic sci-fi.

Recommended image families:

- 16:9 hero: network/service-market landscape;
- 1:1 social card: one headline + protocol strip + one diagram;
- capability card: input → Conway → structured output;
- proof card: one independently verifiable metric with timestamp/source;
- release card: release ID + material buyer-facing change.

## Copy bank

**Primary:** APIs that sell themselves to agents.

**Alternative:** Machine-discoverable services. Machine-native payments. Useful results.

**Commerce:** Your software should be able to buy software.

**Developer:** Skip the subscription. Call the capability.

**Protocol:** Discover with A2A. Pay with x402. Receive structured output.

**Trust:** Runtime truth over marketing claims.

## SEO / GEO / agentic discovery

Maintain one canonical description across structured metadata. Give every flagship service a stable name, canonical URL, concise job-oriented description, schema and example. Use structured WebSite/WebAPI metadata and sitemaps for human/search discovery while keeping OpenAPI and Agent Card semantics authoritative for machine consumers.

Do not duplicate hundreds of thin pages solely for search ranking. Generate public pages only when they contain a real callable capability, useful example or meaningful evidence.

## Weekly growth loop

1. Inspect which capabilities were discovered.
2. Inspect which generated 402 challenges.
3. Inspect which converted to unrelated settled payments.
4. Inspect fulfilment quality, cost and latency.
5. Improve the highest-intent offer with the largest conversion loss.
6. Publish one evidence-backed demo/integration around that offer.
7. Re-check registry and discovery propagation.
8. Retire or de-emphasize offers that attract attention but no economically meaningful demand.

This loop keeps marketing coupled to real economic evidence instead of vanity metrics.
