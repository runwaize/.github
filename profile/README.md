# Runwaize

Runwaize builds the **operations and distribution layer** for AI agents in the real world.

Our ecosystem has four pillars:

- **Supervaize** — the **commercial SaaS** control plane for operating AI agents at scale (missions, jobs, HITL, governance, observability).
- **Supervaizer** — the **open-source** controller/runtime components that connect agents to Supervaize and enforce operational rules.
- **Skills Cookbook** — the skills catalog + curation + sharing layer (import skills, scan them, personalize them, publish libraries).
- **Skills Cookbook Relay** — the **open-source** local bridge that securely delivers curated skills to agents (MCP server, verification, local secrets).

We’re focused on one thing: **making agent capabilities deployable, trustworthy, and manageable**—without turning your agents into credential dumpster fires.

---

## Products

### [Skills Cookbook](skills.runwaize.com)
A user-first skills management layer that helps you turn “random skills from the internet” into a **trusted, organized, shareable library** for you and for your organization.

Core capabilities:
- Import skills (Vercel skills.sh, GitHub, uploads)
- Rate, comment, tag, and group skills into libraries
- Run security checks and attach scan reports
- Clone/personalize/version skills (configuration overlays by default, not forks)
- Manage variables (secrets as references by default)
- Publish libraries to third parties with install/update instructions

### Skills Cookbook Relay (Open Source)
A lightweight local application that connects to Skills Cookbook and makes curated skills available to agents **securely**.

Core capabilities:
- Runs locally (desktop) and exposes a **localhost MCP server**
- Fetches **latest approved** skills/libraries from Skills Cookbook
- Verifies skill artifacts (hash/signature) before serving them to the agent
- Resolves variables and secrets locally (env/keychain/vault references)
- Caches safely and supports updates + revocations
- Keeps Skills Cookbook API credentials out of the agent runtime

### [Supervaize](app.supervaize.com) (Commercial SaaS)
The control plane for AI agent operations:
- Workspaces, missions, jobs
- Human-in-the-loop steps and approvals
- Visibility into agent behavior + outcomes
- Governance and policy scaffolding

### Supervaizer (Open Source)
Open-source controller/runtime components:
- Connect agents to operational tooling
- Collect telemetry and execution traces
- Enforce operational constraints (policy hooks, guardrails) where applicable
- Provide a foundation for integrations with external agents and frameworks
