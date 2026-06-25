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
- Production deployment: pending fresh Cloudflare D1 creation, Worker deployment, DNS/HTTPS verification, Polar checkout secrets, GSC, Bing, IndexNow, public GitHub repo, independent public docs repo, registry update, live browser validation, and SaaS report-center registration.
