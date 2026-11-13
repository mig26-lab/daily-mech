# Anthropic Opens Private Beta for Self-Hosted Claude Managed Agents

**Published: November 13, 2026**

![AI-powered robotic hand interacting with digital interface](https://cdn.pixabay.com/photo/2025/02/25/04/52/ai-generated-9429537_640.jpg)
*Image from Pixabay (free under Pixabay Content License)*

## Introduction

On November 12, 2026, Anthropic launched a private beta for self-hosted Claude Managed Agents. This allows enterprises to run the full agent orchestration stack—harness, sandboxes, credentials, and session history—inside their own cloud or on-premises data centers. The move addresses growing demand for data sovereignty and security in agentic AI deployments while keeping the Claude models themselves external.

Unlike the previously hosted service where Anthropic managed the infrastructure, customers now operate the Managed Agents server, a PostgreSQL database, and the workers that execute shell and file tools. Access remains invitation-only through Anthropic account teams.

## How Self-Hosting Works

The architecture separates the control plane from model inference:

| Component                  | Location                          | Notes                                      |
|----------------------------|-----------------------------------|--------------------------------------------|
| Agent harness & sandboxes  | Customer cloud / on-prem         | Full control plane                         |
| Server, DB, workers        | Customer-operated                | PostgreSQL 16+ for session history         |
| Credentials & secrets      | Customer secrets manager         | Proxy adds them outside sandbox            |
| Model inference            | Anthropic, Bedrock, Google, Microsoft, or gateway | Claude weights stay remote                 |

Developers continue using the same core APIs as the hosted version. Features such as webhooks and scheduled runs are not yet available in the self-hosted edition, and existing hosted agents cannot be migrated automatically.

## Security and Compliance Benefits

By keeping session history, credentials, and tool execution local, organizations can enforce network allow-lists, export OpenTelemetry logs, and meet strict data-residency requirements. Zero Data Retention agreements can still apply to model calls. Anthropic states it has no remote access to the customer-run server.

This is particularly relevant for regulated industries (finance, healthcare, government) that want agent capabilities without sending internal context or tool outputs to a third-party host.

## Industry Context and Outlook

The beta arrives as AI agents move from demos into production workflows. Competitors are also expanding agent offerings—Google with Gemini agentic features, OpenAI with ChatGPT Wallet and enterprise agents, and Meta with cost-efficient models like Muse Ember. Anthropic’s self-hosting option differentiates on control and compliance rather than pure model performance.

Limitations remain: the private beta status, lack of public pricing for the server component, and the fact that inference still leaves the customer network. Wider general availability timing has not been disclosed.

## Conclusion

Self-hosted Claude Managed Agents give enterprises a practical path to deploy long-running, tool-using agents under their own security perimeter. While model inference remains external, the shift of the control plane and data stores significantly reduces data-exposure risk. Organizations evaluating agent platforms should assess this beta against their compliance needs and compare total cost of ownership once pricing details emerge.

## Sources and References

1. Anthropic announcement: Operate Claude Managed Agents inside your security perimeter (November 12, 2026)
2. Help Net Security, 4sysops, i10X, CellCog, and TokenPost coverage of the private beta
3. Anthropic platform documentation on deployment tiers and security model
4. Related enterprise AI agent news from November 2026

**Helpful Tip:** Contact your Anthropic account team early if you have strict data-residency or audit requirements—beta access is gated and migration from hosted agents is not automatic.
