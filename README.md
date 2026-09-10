# awesome-x402-mcp-services

Curated list of **hosted MCP services** that charge per call with [x402](https://www.x402.org) — no account, no API key. Same shape as Recall Kitchen: a real product you can point an MCP client at and pay USDC when a tool needs it.

This is not a directory of crypto trading bots, token screens, payment routers, or 50-tool utility packs.

### Table of Contents

* [Search](#search)
* [Business data](#business-data)
* [Marketing](#marketing)
* [Monitoring](#monitoring)
* [Official records](#official-records)

### Helpful Links

* [x402/MCP Developers](#developers)

## Services

### Search

* [Recall Kitchen](https://recallkitchen.com/docs/#mcp) — product, food, and vehicle recall search. Hosted MCP, x402 USDC on Base, no account. [MCP](https://app.recallkitchen.com/mcp)

### Web access

* [CyberWareX Agent Web-Access](https://web.cyberwarex.com) - live web pages for agents: JS-rendered fetch to markdown/text/html, CSS-selector extract, screenshot, PDF. Hosted MCP at `https://web.cyberwarex.com/mcp` (streamable HTTP, no key). Unpaid tool calls return the x402 invoice (USDC on Base, $0.002-0.005); pay and retry with `x_payment`.

### Business data

* [Sirenic](https://api.sirenic.eu) — French and European company registry: search, profiles, KYB, sanctions, filed financials. Hosted MCP at `https://api.sirenic.eu/mcp`. Unpaid calls return HTTP 402 (USDC/EURC on Base).

### Marketing

* [Social Intel](https://socialintel.dev) — Instagram influencer search by niche, country, city, and follower count. Hosted MCP at `https://socialintel.dev/mcp`. Paid `search_leads` via x402; `demo=true` is free.

### Monitoring

* [Longwatch](https://longwatch.dev) — durable watches on public pages, RSS, and SEC EDGAR filings, with resumable cursors. Hosted MCP at `https://longwatch.dev/mcp`. Paid tools return HTTP 402 (USDC on Base); free demo at `/demo`.

### Official records

* [Truth Bear (GAUGE)](https://api.truthbear.co) — official-series records (FRED, USGS, SEC EDGAR, NOAA, EPA, and similar) with a source URL and a recomputable record hash. Hosted MCP at `https://api.truthbear.co/mcp`. Coverage tools are free; paid records go through an x402 challenge.

## Developers

* [xpaysh/awesome-x402](https://github.com/xpaysh/awesome-x402)
  * [Quick Start Guides](https://github.com/xpaysh/awesome-x402?tab=readme-ov-file#-quickstart-guides)
  * [Example Applications](https://github.com/xpaysh/awesome-x402?tab=readme-ov-file#-example-applications)
* [xpaysh/awesome-mcp-monetization](https://github.com/xpaysh/awesome-mcp-monetization)
* [xpaysh/awesome-agentic-economy](https://github.com/xpaysh/awesome-agentic-economy)

## Contributing

To add a commercial service (no payment required for submission):

1. **Hosted MCP** — a public streamable-HTTP MCP URL that answers `initialize` / `tools/list` without an API key.
2. **x402** — a paid tool or route returns HTTP 402 (or an MCP payment error with x402 accepts). No account required.
3. **A real product** — one job an agent would hire you for (search, registry data, filings, monitoring, and so on). Deployed today, not a Cloudflare tunnel, `localhost`, Tailscale, or `nip.io` IP.
4. **Not a fit** — crypto/trading/DeFi/token screens, generic 20–500 tool dumps, x402 routers/marketplaces/facilitators, games, or SDKs. Put SDKs and awesome-lists under Developers only if they are documentation, not a self-listing.

Open a pull request that adds one bullet under the matching Services section:

`- [Service Name](https://link-to-service) - Brief description.`

In the PR body, include the MCP URL and how an unpaid call produces 402. We will probe those before merging.
