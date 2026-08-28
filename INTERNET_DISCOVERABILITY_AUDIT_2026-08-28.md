# Conway Replicatio — Internet Discoverability Audit

Audit date: 2026-08-28

## Executive verdict

Conway's **machine-discovery architecture is strong**, but its **external propagation and human-search authority lag the live origin**. The canonical Worker and GitHub mirror expose a broad standards-based discovery graph, while several independent directories still serve older cached metadata. This is a distribution/freshness gap, not evidence that the canonical runtime is stale.

No directory listing, scanner result, uptime observation, crawler hit or canary is treated as revenue. At the time of this audit there is no credible evidence of an unrelated external payer with both successful settlement and successful fulfilment.

## Canonical public identity

- Name: `Conway Replicatio`
- Category: autonomous A2A economic agent / machine-service merchant
- Canonical origin: `https://conway-replicatio-cloudflare.nikitamakiel1.workers.dev`
- Canonical Agent Card: `/.well-known/agent-card.json`
- A2A JSON-RPC: `/a2a/v1`
- OpenAPI: `/openapi.json`
- x402 discovery: `/.well-known/x402`
- Runtime capability authority: `/api/public/capabilities`
- Human machine documentation: `/machine`

## Current channel matrix

| Channel | Current observation | Assessment | Required action |
| --- | --- | --- | --- |
| Canonical Worker | R119 identity/discovery surfaces are live; recent synchronization closure separates stable public identity from volatile telemetry | Strong | Preserve canonical origin and keep buyer-facing content useful and crawlable |
| GitHub Agent Card mirror | Current mirror uses projection schema v2 / `r119-sync-closure-v2`; both Agent Card paths are machine-managed | Strong | Do not manually edit Agent Card JSON; keep human docs current |
| A2A Registry — Worker listing | Independent registry still serves older cached Conway metadata and remains unclaimed | Stale external cache | Refresh/claim the existing listing only after canonical stability is proven; do not create a duplicate |
| A2A Registry — GitHub-backed listing | Independent registry still exposes older cached metadata despite a newer GitHub source | Stale external cache | Allow/trigger recrawl after stability; retain GitHub mirror as stable source |
| Agenstry | Independent listing observes Conway alive with A2A 1.0 and broad skills, but reports `Live JSON-RPC = 0` and 80% average quality | Material interoperability signal | Validate free standards-compatible `SendMessage`; support harmless legacy method aliases if needed without weakening payment/auth |
| x402lint / x402scan | Last independently visible cached grade remains B, with Protocol 96, Docs 59, Standing 98 and x402scan visibility | Strong protocol, stale/weak docs measurement | Run a fresh scan only after the next discovery closure is live; fix exact findings, not guessed score targets |
| Bing / Copilot discovery | Worker already implements sitemap/robots and inherited IndexNow notification | Strong technical base | Keep canonical URLs, useful visible content, internal links and accurate freshness; use Bing Webmaster Tools for first-party measurement if ownership is configured |
| Google / AI Search | Standard crawl/index/SEO rules apply; no special AI-only indexing mechanism is required | Human-search authority still developing | Improve visible root content, title/description, internal linking, structured identity and useful non-commodity documentation; measure in Search Console when ownership is configured |
| GitHub search/backlinks | Public mirror provides a stable indexable technical identity and integration documentation | Useful supporting authority | Publish evidence-led technical content and integration examples rather than keyword-stuffed pages |

## What is already technically strong

### A2A discovery
Conway publishes a canonical Agent Card with a JSON-RPC interface and explicit A2A 1.0 semantics. The public mirror provides a stable source for GitHub-backed registries.

### x402 discovery
Conway publishes payable HTTP operations, OpenAPI payment metadata and `/.well-known/x402` discovery. Runtime HTTP 402 payment requirements remain authoritative over static descriptions.

### Search/crawler discovery
Conway publishes a canonical human root, sitemap, robots policy, favicon, structured WebSite identity, OpenAPI, `agents.txt`, `agents.json`, `llms.txt`, Agent Skills and RFC 9727 API-catalog discovery.

### Synchronization integrity
The current public projection explicitly excludes volatile ranking scores, canary timestamps, external-registry check timestamps and operational synchronization telemetry. Current evidence remains on dedicated runtime endpoints rather than churning the long-lived Agent Card.

## Highest-priority remaining weaknesses

### 1. Human commercial compression
The Worker should lead with the buyer job rather than internal architecture. The preferred message hierarchy is:

**APIs that sell themselves to agents.**

**Machine-discoverable web intelligence. Pay per call with x402. Structured results.**

Then show a direct path:

`DISCOVER → 402 → PAY → RESULT`

and a small flagship offer set before exposing the long-tail catalogue.

### 2. A2A callable compatibility
Agenstry's `Live JSON-RPC = 0` deserves direct treatment. Conway has a real A2A JSON-RPC implementation, so a zero probe result is likely to be caused by request-shape, method-version or generic-probe incompatibility. The correct fix is compatibility at the protocol edge, not fake health metadata.

A compatibility layer may safely normalize older A2A method names such as `message/send` to current v1 `SendMessage` where mapping is unambiguous. A generic valid message with no paid intent may fall back to free capability discovery. Such a probe must never create paid execution or revenue truth.

### 3. Agent Card size and internal-state density
Even after volatile telemetry removal, the flagship Agent Card still carries extensive inherited implementation/release detail. Machine clients need stable identity, interfaces, representative skills, payment/discovery pointers and truth boundaries — not the entire internal lineage. The complete live inventory belongs at `/api/public/capabilities` and OpenAPI.

### 4. External cache freshness
A2A Registry currently trails the canonical source. Duplicate registrations would make identity fragmentation worse. Refresh/claim the existing entries only after the canonical projection is stable across reconciliation cycles.

### 5. Human search authority
Exact-brand searches currently lean heavily on independent directories rather than the canonical Worker itself. Search engines need useful visible content and external references, not only machine manifests. The Worker root should therefore have a strong page title, concise description, crawlable buyer-oriented copy, internal links and consistent structured identity.

## Search-engine / AI-search policy

### Google
Google's current guidance for generative AI features says normal SEO foundations continue to apply. Useful, unique, crawlable content and standard Search indexing are the basis for AI Overviews/AI Mode visibility. `llms.txt` can remain useful for other machine ecosystems but must not be treated as a Google ranking shortcut.

### Bing / Copilot
Bing's current Webmaster Guidelines emphasize canonical URLs, crawlable internal links, XML sitemaps, IndexNow and accurate content/freshness. Bing's AI Performance reports can measure citation visibility across supported AI experiences when the site is verified in Bing Webmaster Tools.

## Content strategy

Publish material that creates real reference value:

1. exact capability demonstrations with input/output and live route;
2. minimal A2A and x402 integration recipes;
3. transparent protocol/conformance reports;
4. evidence-led release notes explaining buyer-facing changes;
5. benchmarks only when methodology and measured data exist;
6. public discovery-status reports that distinguish canonical truth from third-party cache state.

Do **not** generate hundreds of thin capability pages, synthetic reviews, fake testimonials, fake transaction graphics, invented customer logos, fictitious discounts or manufactured backlinks.

## Commercial funnel to instrument

`external discovery → canonical manifest/page → operation/schema view → 402 challenge → valid payment attempt → settled unrelated payment → successful fulfilment → repeat buyer → realized contribution margin`

Every stage should be measured separately. A scanner hit or registry suggestion belongs only to the discovery layer.

## Counteraudit

A discoverability improvement fails if any of the following becomes true:

- marketing copy promises guaranteed sales, profit or future demand;
- registry/cache state is presented as canonical runtime truth;
- canary verification is described as customer validation;
- x402/A2A names are presented as endorsements or partnerships;
- search-oriented pages contain no unique callable capability, example or evidence;
- a generic A2A health probe can accidentally invoke a paid operation;
- a compatibility alias bypasses existing payment or authorization controls;
- volatile operational state re-enters the stable Agent Card;
- the Worker and GitHub mirror advertise conflicting identity or capability populations;
- revenue is recorded without both unrelated settlement and successful fulfilment evidence.

## Readiness interpretation

Conway should be judged on separate axes rather than one vanity score:

- **Machine discoverability:** protocol surfaces, schemas and canonical identity.
- **Human/search discoverability:** crawlability, buyer clarity, useful content and authority.
- **External propagation:** third-party registry/index freshness.
- **Invocation quality:** whether independent clients can actually call free discovery and paid routes correctly.
- **Commercial proof:** unrelated settled-and-fulfilled usage and repeat demand.

The first four can be engineered and measured. The fifth cannot be manufactured by marketing.
