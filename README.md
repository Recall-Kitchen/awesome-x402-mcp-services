# awesome-x402-mcp-services

Curated list of **hosted MCP services** that charge per call with [x402](https://www.x402.org) — no account, no API key. Same shape as Recall Kitchen: a real product you can point an MCP client at and pay USDC when a tool needs it.

This is not a directory of crypto trading bots, token screens, payment routers, or 50-tool utility packs.

### Table of Contents

* [Search](#search)
* [News](#news)
* [Web access](#web-access)
* [Business data](#business-data)
* [Content](#content)
* [Marketing](#marketing)
* [Monitoring](#monitoring)
* [Official records](#official-records)
* [Data utilities](#data-utilities)
* [Verification](#verification)

### Helpful Links

* [x402/MCP Developers](#developers)

## Services

### Search

* [Recall Kitchen](https://recallkitchen.com/docs/#mcp) — product, food, and vehicle recall search. Hosted MCP, x402 USDC on Base, no account. [MCP](https://app.recallkitchen.com/mcp)

### News

* [askzephy news feed](https://audit.askzephy.com) — Google News coverage per topic query (brand, competitor, person, exact phrase): normalized rows with title, article URL, publisher, publish time, snippet; 10 locales. Hosted MCP at `https://audit.askzephy.com/mcp` (streamable HTTP, no key). Unpaid `google_news_feed` calls return HTTP 402 (USDC on Base, $0.01); sign the payment and retry in the call `_meta`.
* [Briefing Service](https://wholemind.tech/briefing/index.html) — hourly LLM-ranked news briefings (AI, frontier labs, markets, US and world news, sports) from ~100 feeds: lead, why-it-matters, key points and duplicates merged, as JSON or rendered e-ink pages. Hosted MCP at `https://briefing-service.wholemind.workers.dev/mcp` (streamable HTTP, no key); `initialize` and `tools/list` are free, `tools/call` returns the x402 challenge (USDC on Base, $0.005 per call) after a small free daily quota.

### Web access

* [agdata](https://agdata.shveik.dev) — web data for agents: any URL as clean Markdown, screenshots, web search, Google Maps and Amazon reviews, job listings, news, social posts and comments, YouTube transcripts. Hosted MCP at `https://agdata.shveik.dev/mcp` (streamable HTTP, no key). Unpaid tool calls return an x402 payment error (stablecoins on Base, Polygon or Solana, MPP on Base); sign the payment and retry in the call `_meta`. A scrape that fails is not charged.
* [agproxy](https://agproxy.shveik.dev) — residential proxy traffic and a raw fetch for agents, with country targeting and sticky sessions. Hosted MCP at `https://agproxy.shveik.dev/mcp` (streamable HTTP, no key). Unpaid tool calls return an x402 payment error (stablecoins on Base or Polygon, MPP on Base); sign the payment and retry in the call `_meta`.
* [APEX Web](https://apexfaucet.xyz/explained/#agents) — web pages for agents from a real headless Chrome: one page rendered with JavaScript run ($0.009), up to 25 pages of a site in one call with robots.txt obeyed ($0.14), or up to 10 plain pages as clean text ($0.003). Hosted MCP at `https://apexfaucet.xyz/api/mcp/web`. Unpaid calls return the x402 terms (USDC on Arc, Base or Solana, or XNT on X1).
* [CyberWareX Agent Web-Access](https://web.cyberwarex.com) — live web pages for agents: JS-rendered fetch to markdown/text/html, CSS-selector extract, screenshot, PDF. Hosted MCP at `https://web.cyberwarex.com/mcp` (streamable HTTP, no key). Unpaid tool calls return the x402 invoice (USDC on Base, $0.002-0.005); pay and retry with `x_payment`.
* [PageWire](https://pagewire.dev) — web pages for agents without a browser: one public URL to clean Markdown with title, description and links ($0.01), page metadata — OpenGraph, Twitter card, JSON-LD, canonical, language, icons ($0.005), or a page plus up to 4 same-host linked pages, optionally under a path prefix ($0.03). Hosted MCP at `https://pagewire.dev/mcp` (streamable HTTP, no key). Unpaid tool calls return an MCP payment error with x402 accepts (USDC on Base or Solana); sign and retry in the call `_meta`. Pages that fail to load are not charged.
* [Vend](https://extract.paypercall.dev) — paid web tools for agents: page-to-clean-text web extraction, web search, link checker, domain info, geoip, nano-info, YouTube transcripts. Hosted MCP at `https://extract.paypercall.dev/mcp` (streamable HTTP, no key). Unpaid tool calls return HTTP 402 settled in **Nano (XNO)** via x402 exact — instant, feeless, self-facilitated PAYMENT-SIGNATURE, no USDC/Base.

### Business data

* [AgentPay](https://agentpay.help) — Insurance lead and business-document analysis: classify an inbound insurance lead, extract structured fields from the form or email, and return a claims/lead summary. Hosted MCP at `https://agentpay.help/mcp` (streamable HTTP, no key); unpaid tool calls return HTTP 402 (USDC on Base, $0.005-$0.10). JSON in, JSON out.
* [Saymon RU Data API](https://payforapi.com) — Russian company registry (EGRUL) and KYB dossiers, official Russian series (Central Bank rates, MOEX quotes), and Runet search. Hosted MCP at `https://payforapi.com/mcp`. Unpaid tool calls return an x402 payment error (USDC on Base, $0.005-$0.05); sign the payment and retry in the call `_meta`.
* [Sirenic](https://api.sirenic.eu) — French and European company registry: search, profiles, KYB, sanctions, filed financials. Hosted MCP at `https://api.sirenic.eu/mcp`. Unpaid calls return HTTP 402 (USDC/EURC on Base).
* [Vérif Entreprise FR](https://api-production-24833.up.railway.app) — French company verification (KYB) by SIREN from official open data (Annuaire des Entreprises, BODACC, ADEME): legal status, insolvency-procedure state, RGE certifications and an explained verdict with documented signal codes. Hosted MCP at `https://api-production-24833.up.railway.app/mcp` (streamable HTTP, no key); tools `verifier_entreprise` ($0.01), `rechercher_entreprise` ($0.002), `qualifications_rge` ($0.01). Unpaid tool calls return an MCP payment error with x402 accepts (USDC on Base or Solana); failed lookups are never charged.

### Content

* [Penny Press](https://www.pennypress.org) — essays on freedom, economics and philosophy: free for humans to read, pay-per-read for AI agents. Hosted MCP at `https://www.pennypress.org/mcp` (streamable HTTP, no key). Unpaid tool calls return HTTP 402 (USDC on Base, $0.01–$0.05 per essay); sign the payment and retry.

### Marketing

* [Social Intel](https://socialintel.dev) — Instagram influencer search by niche, country, city, and follower count. Hosted MCP at `https://socialintel.dev/mcp`. Paid `search_leads` via x402; `demo=true` is free.

### Monitoring

* [Longwatch](https://longwatch.dev) — durable watches on public pages, RSS, and SEC EDGAR filings, with resumable cursors. Hosted MCP at `https://longwatch.dev/mcp`. Paid tools return HTTP 402 (USDC on Base); free demo at `/demo`.

### Official records

* [Agent402 SEC Filings](https://agent402.tools/mcp/sec) — SEC EDGAR over MCP: company lookup, filings, full-text search, Form 4 insider trades, 13F holdings and XBRL financials, plus grounded filing, insider and fund reports. Hosted MCP at `https://agent402.tools/mcp/sec`; every tool is paid per call in USDC and an unpaid call answers a payment challenge.
* [Truth Bear (GAUGE)](https://api.truthbear.co) — official-series records (FRED, USGS, SEC EDGAR, NOAA, EPA, and similar) with a source URL and a recomputable record hash. Hosted MCP at `https://api.truthbear.co/mcp`. Coverage tools are free; paid records go through an x402 challenge.
* [fitze x402 tools](https://fitze-x402-seller.app.workbuddy.host) — official-record and due-diligence lookups for agents: SEC EDGAR full-text search, FDA recall reports, USGS earthquakes, domain dossier (RDAP + DNS + certificate transparency), and GitHub repo due diligence with contributors, archived flag and health score. Hosted MCP at `https://fitze-x402-seller.app.workbuddy.host/mcp` (streamable HTTP, no key); `initialize` and `tools/list` are free, an unpaid `tools/call` returns HTTP 402 settled in USDC on Base ($0.005-$0.25 per tool, one tool free).

### Data utilities

* [Penniless Data Utilities](https://penniless-json-repair.sjaman.workers.dev) — nine deterministic AI-agent data and lookup utilities (JSON repair, YAML→JSON, cron next-run, text diff/extract, HTML→text, RDAP WHOIS, DNS-over-HTTPS, GitHub repo stats, email validation). Hosted MCP at `https://penniless-json-repair.sjaman.workers.dev/mcp` (streamable HTTP, no key); `tools/list` is free. Each tool is $0.001 USDC per call on Base via x402 v2; an unpaid `tools/call` returns a 402 payment-required error whose data carries the signed-payment requirements. Pay and retry with the payment in the call `_meta`. [Discovery](https://penniless-json-repair.sjaman.workers.dev/.well-known/agent.json)

### Verification

* [crosscheck](https://crosscheckapi.com/llms.txt) - independent checks an agent runs before acting: `skillcheck` reviews a skill or MCP server's files before install (free when already scanned), `accept` checks another agent's deliverable against its task before payment, `check` reviews a draft before its human sees it. Signed receipts. Hosted MCP at `https://crosscheckapi.com/mcp` (streamable HTTP, no key). Unpaid tool calls return an x402 PaymentRequired (USDC on Base; free test USDC on Base Sepolia).
* [Settled](https://settled.tools/for-agents) — checks an x402 endpoint before an agent pays it: whether the payTo in its quote matches what Settled's own probe sees, whether Settled's real USDC test purchase came back with content, the seller's on-chain settlement record and paying agents' reports, with a signed pay / caution / avoid answer. Hosted MCP at `https://settled.tools/mcp` (streamable HTTP, no key). `settled_check` is free for 300 calls a day; `settled_watch` (10 days of monitoring for one endpoint, $1) answers an unpaid call with an x402 PaymentRequired (USDC on Base).

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

`* [Service Name](https://link-to-service) — Brief description.`

Keep sections alphabetized by service name. In the PR body, include the MCP URL and how an unpaid call produces 402. We will probe those before merging.
