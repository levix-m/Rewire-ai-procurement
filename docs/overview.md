# Overview

## What this repository is

**Procurement Agents** is a structured, collaborative library of procurement-focused AI agents. Each agent is documented with prompts, workflows, examples, evaluation criteria, and a place for implementation code—so teams can adopt, extend, or replace behavior without losing consistency.

The goal is not to ship a single product, but to provide a **governed pattern** for how procurement agents are named, described, versioned in metadata, and discovered through a central registry.

## Who it is for

- **Category and sourcing leaders** who want reusable playbooks and agent definitions aligned to real workflows.
- **Platform and engineering teams** integrating agents into ERP, P2P, CLM, or custom orchestration layers.
- **Risk, compliance, and security** stakeholders who need predictable documentation and review surfaces.

## How it differs from “agent lists”

Collections that only link to external projects optimize for **discovery**. This repository optimizes for **repeatability**:

- Every agent follows the **same folder contract**.
- **Metadata** in `agent.yaml` and the **registry** stay aligned for search, reporting, and ownership.
- **Governance** and **evaluation** expectations are explicit, not implied.

## Repository map (quick)

| Area | Role |
|------|------|
| `agents/` | Domain-organized agent definitions (the library). |
| `templates/agent-template/` | Copy-paste starting point for new agents. |
| `registry/` | Index and categories for discoverability and governance. |
| `shared/` | Cross-cutting prompts, schemas, tools, utilities, datasets. |
| `docs/` | How the library works and how to contribute consistently. |
| `governance/` | Security, compliance, review, and approved patterns. |

## Principles

1. **Structure over sprawl** — If it does not fit the agent contract, it belongs in `shared/` or `docs/`, not a one-off folder.
2. **Prompt-first or code-first** — Implementations may be prompts, workflows, or code; the documentation shell stays the same.
3. **Evaluations are first-class** — Every agent ships criteria and a test plan, even when automation is still roadmap.

## Next steps

- Read [architecture.md](./architecture.md) for how pieces connect.
- Read [onboarding.md](./onboarding.md) to add or change an agent.
- Read [evaluation-framework.md](./evaluation-framework.md) before changing behavior that affects buyers or suppliers.
