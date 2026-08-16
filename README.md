# awesome-x402-mcp-services

Curated list of awesome commercial services that require x402 payments and use MCP. No accounts required. Payments via x402 for MCP tools.

### Table of Contents

- [Governance & Safety](#governance--safety)
- [Search](#search)

### Helpful Links

- [x402/MCP Developers](#developers)

## Services

### Governance & Safety

- [Fieldproof Policy Gate](https://policy-gate.3labsio.workers.dev/mcp) - Decides whether an agent action is permitted before it happens. `policy_check` returns allow / require_approval / deny against a tiered default-deny policy (bring your own inline), with the matched rule and rationale so the verdict is auditable. `policy_example` and `policy_rules` are free tools, so an agent can evaluate the service inside its own client before spending anything. No model in the hot path: same input, same verdict. $0.005 USDC on Base, no account or API key.

### Search

- [Recall Kitchen](https://recallkitchen.com/docs/#mcp) offers search for product, food, and vehicle recalls.

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
