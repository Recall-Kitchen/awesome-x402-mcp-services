# awesome-x402-mcp-services

Curated list of awesome commercial services that require x402 payments and use MCP. No accounts required. Payments via x402 for MCP tools.

### Table of Contents

- [Search](#search)

### Helpful Links

- [x402/MCP Developers](#developers)

## Services

### Search

- [Recall Kitchen](https://recallkitchen.com/docs/#mcp) offers search for product, food, and vehicle recalls.

### Payment Verification / Trust

- [Revenue Dojo Agent Payment Receipt and Mandate Verifier](https://x402.167-172-95-184.nip.io) - x402-paid MCP gateway and agent-commerce trust API for receipt verification, mandate checks, and x402 launch audits. Evidence: `POST /mcp/call`, `POST /receipt/verify`, `POST /mandate/verify`, and `GET /audit/x402` are x402-gated; discovery manifests are at `/.well-known/x402` and `/openapi.json`.

## Developers

- [xpaysh/awesome-x402](https://github.com/xpaysh/awesome-x402)
   - [Quick Start Guides](https://github.com/xpaysh/awesome-x402?tab=readme-ov-file#-quickstart-guides)
   - [Example Applications](https://github.com/xpaysh/awesome-x402?tab=readme-ov-file#-example-applications)
- [xpaysh/awesome-mcp-monetization](https://github.com/xpaysh/awesome-mcp-monetization)
- [xpaysh/awesome-agentic-economy](https://github.com/xpaysh/awesome-agentic-economy)

## Contributing

To add your commercial service to this curated list (no payment required for submission):

1. Ensure your service requires x402 payments and integrates with MCP.
2. Open a pull request with your service added to the Services section in the format: `- [Service Name](https://link-to-service) - Brief description.`
3. Provide evidence or details on how it uses x402 payments and MCP.
4. Your PR will be reviewed for inclusion.
