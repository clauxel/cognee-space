# WEBSITE_CHANGELOG

## 2026-06-25

- Scope: initial build for `cognee.space` using the open-source-code website build workflow.
- Repo input: `topoteretes/cognee`.
- Positioning: independent, unofficial Cognee AI memory deployment planner rather than an official service clone.
- Implemented pages: homepage planner preview, AI memory, knowledge graph RAG, agent memory, MCP memory server, self-host Cognee, pricing, checkout, success, cancel, docs/source notes, privacy, terms, changelog, and 404.
- Implemented assets: upstream memory graph hero bitmap, favicon, web manifest, robots.txt, sitemap.xml, llms.txt, product.json, and facts JSON endpoint.
- Implemented runtime: Cloudflare Worker static serving, canonical redirect logic, `/api/runtime`, `/api/planner`, `/api/analytics`, `/api/checkout`, `/api/access`, and `/.well-known/cognee-space.json`.
- Implemented payment rule: independent `/pricing/` page, Annual/Monthly tabs, Annual selected by default, Annual 50% cheaper than Monthly, one-time/no automatic renewal copy, own-domain checkout API, Polar checkout wiring, and paid planner gate.
- Implemented data rule: `/api/analytics` writes durable events to Cloudflare D1 when `ANALYTICS_DB` is bound and reports `stored:true` only after D1 insertion.
- Local verification: `npm test` passed for static SEO, one H1 per page, no visible outbound CTA links, pricing-first flow, paid planner gate, D1 analytics mock, Polar checkout wiring, access-token unlock, facts JSON, 404 handling, and stale-template checks.
- GitHub: public repositories `clauxel/cognee-space` and `clauxel/cognee-space-docs` were created and pushed.
- Cloudflare: Worker `cognee-space` deployed with D1 database `cognee-space-analytics` (`43ba68cd-a7b2-401a-a462-d27219c524d3`) and workers.dev returned 200.
- Polar: six checkout links were created or reused and stored in Cloudflare Worker secrets; `/api/runtime` reported `paymentConfigured:true`; all six plan/billing checkout API combinations returned hosted Polar checkout URLs.
- Production custom-domain status: `cognee.space` and `www.cognee.space` are configured in Cloudflare routes and DNS, and registrar nameservers were updated to `archer.ns.cloudflare.com` and `sydney.ns.cloudflare.com`.
- Production blocker: external DNS resolvers return DNSSEC validation failure because Cloudflare DNSSEC is disabled while a DS chain still exists for `cognee.space`. Apex/www HTTPS cannot be marked live until Owner authorizes DNSSEC/DS repair at the registrar/Cloudflare boundary.
- Search submission: GSC, Bing Webmaster, and IndexNow were not submitted because the canonical sitemap on `https://cognee.space/sitemap.xml` is not resolvable under validating DNS. No old search-submission result was reused.
