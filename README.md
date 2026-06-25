# Cognee Space

Independent, unofficial Cognee AI memory deployment planner for `cognee.space`.

The site helps teams plan persistent AI memory, knowledge graph RAG, MCP memory server access, feedback loops, and self-hosted Cognee deployment. It does not provide official Cognee support and does not send primary CTAs to upstream or third-party product pages.

## Source Notes

- Official site: https://www.cognee.ai/
- Official docs: https://docs.cognee.ai/
- Upstream repo: https://github.com/topoteretes/cognee
- License summary used by this site: Apache-2.0.

## Pages

- `/` - paid planner preview and product entity
- `/ai-memory/` - persistent agent memory planning
- `/knowledge-graph-rag/` - graph RAG rollout planning
- `/agent-memory/` - agent workflow memory boundaries
- `/mcp-memory-server/` - MCP memory server checklist
- `/self-host-cognee/` - self-host checklist
- `/pricing/` - Annual/Monthly packages with Annual selected by default
- `/checkout/` - own-domain Polar checkout start
- `/docs/` - source notes and page matrix

## Verification

Run:

```bash
npm test
```

Validation covers static SEO, canonical and Open Graph URLs, one H1 per page, no visible outbound CTA links, D1 analytics storage behavior, paid planner gate, Polar checkout wiring, access-token unlock, facts JSON, 404 handling, pricing tabs, and stale-template text.

Search launch evidence will be stored in `search-submission-result.json` after production deployment and fresh GSC/Bing/IndexNow submission.

## Deployment

Cloudflare Worker deployment is configured in `wrangler.toml` for `cognee.space` and `www.cognee.space`. Production completion requires Cloudflare zone/DNS/HTTPS, D1 binding, Polar checkout secrets, apex/www verification, GSC, Bing, IndexNow, public GitHub repo, independent docs repo, registry update, and live user-flow validation.
