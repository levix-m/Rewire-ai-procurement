# Rewire AI procurement

A **structured, collaborative library** of procurement agents—organized by workflow domain, documented for enterprise use, and designed to scale without turning into an unmaintainable link farm.

**Repository:** [github.com/levix-m/rewire-ai-procurement](https://github.com/levix-m/rewire-ai-procurement)

This repository takes inspiration from large “agent project” lists on discoverability, then adds **consistent structure**, **explicit metadata**, and **governance hooks** so many contributors can extend the same system over years.

---

## Why this exists

Procurement work spans **strategy**, **sourcing**, **negotiation**, **performance management**, and **value preservation**. Agents should mirror that reality: small, composable capabilities with clear inputs, outputs, owners, and evaluation criteria—not one opaque chatbot.

**Core promises**

- **Same skeleton everywhere** — every agent uses an identical folder contract.
- **Registry-first discovery** — `registry/agents-index.yaml` is the catalog; README tables stay in sync.
- **Prompt-first, workflow-first, or code-first** — implement however you need; documentation stays portable.
- **Growth without mess** — shared assets and governance docs channel reuse and review.

---

## Browse by domain

| Domain | Focus | Folder |
|--------|--------|--------|
| **Strategy** | Spend visibility, category strategy, cost intelligence, data foundations | [`agents/strategy/`](agents/strategy/) |
| **Sourcing** | Market engagement, RFx execution, guided sourcing plays | [`agents/sourcing/`](agents/sourcing/) |
| **Negotiation** | Deal preparation, commercial scenarios, fast repricing support | [`agents/negotiation/`](agents/negotiation/) |
| **Performance management** | Supplier governance, spend controls, savings realization, KPI insight | [`agents/performance-management/`](agents/performance-management/) |
| **Value preservation** | Contract intelligence, invoice-to-contract alignment | [`agents/value-preservation/`](agents/value-preservation/) |

---

## Agent catalog

| Agent | Domain | Path |
|--------|--------|------|
| Spendscape | Strategy | [`agents/strategy/spendscape`](agents/strategy/spendscape) |
| Source AI | Strategy | [`agents/strategy/source-ai`](agents/strategy/source-ai) |
| Category Strategy Agent | Strategy | [`agents/strategy/category-strategy-agent`](agents/strategy/category-strategy-agent) |
| SpendSculptor | Strategy | [`agents/strategy/spendsculptor`](agents/strategy/spendsculptor) |
| ICM (Input Cost Monitor) | Strategy | [`agents/strategy/icm-input-cost-monitor`](agents/strategy/icm-input-cost-monitor) |
| **S4G** | Sourcing | [`agents/sourcing/s4g`](agents/sourcing/s4g) |
| eRFX Agent | Sourcing | [`agents/sourcing/erfx-agent`](agents/sourcing/erfx-agent) |
| RFX Creator | Sourcing | [`agents/sourcing/rfx-creator`](agents/sourcing/rfx-creator) |
| Negotiation Coach | Negotiation | [`agents/negotiation/negotiation-coach`](agents/negotiation/negotiation-coach) |
| Rapid Repricing | Negotiation | [`agents/negotiation/rapid-repricing`](agents/negotiation/rapid-repricing) |
| Supplier Performance Management | Performance management | [`agents/performance-management/supplier-performance-management`](agents/performance-management/supplier-performance-management) |
| Spend Control Tower | Performance management | [`agents/performance-management/spend-control-tower`](agents/performance-management/spend-control-tower) |
| Savings Tracker | Performance management | [`agents/performance-management/savings-tracker`](agents/performance-management/savings-tracker) |
| Supplier Performance Cockpit | Performance management | [`agents/performance-management/supplier-performance-cockpit`](agents/performance-management/supplier-performance-cockpit) |
| Contract AI | Value preservation | [`agents/value-preservation/contract-ai`](agents/value-preservation/contract-ai) |
| Invoice to Contract Compliance | Value preservation | [`agents/value-preservation/invoice-to-contract-compliance`](agents/value-preservation/invoice-to-contract-compliance) |

> Full machine-readable metadata: [`registry/agents-index.yaml`](registry/agents-index.yaml)

---

## Standard agent structure

Every agent uses the same layout so tools, humans, and future CI can rely on paths:

```text
agent-name/
├── README.md
├── agent.yaml
├── prompts/
│   ├── system.md
│   └── tasks.md
├── workflows/
│   └── default-workflow.md
├── examples/
│   ├── sample-input.md
│   └── sample-output.md
├── evals/
│   └── evaluation-criteria.md
├── tests/
│   └── test-plan.md
├── src/
│   └── README.md
└── assets/
    └── README.md
```

**Add a new agent:** copy [`templates/agent-template/`](templates/agent-template/), rename the folder, replace starter content, then register it. Step-by-step: [`CONTRIBUTING.md`](CONTRIBUTING.md).

---

## What each top-level area is for

| Path | Purpose |
|------|---------|
| [`agents/`](agents/) | The live library—one folder per agent under its procurement domain. |
| [`templates/agent-template/`](templates/agent-template/) | Golden scaffold; duplicate this for every new agent. |
| [`shared/`](shared/) | Cross-cutting prompts, schemas, tool docs, utilities, datasets—reuse deliberately. |
| [`registry/`](registry/) | `agents-index.yaml`, `categories.yaml`, maturity and metadata rules. |
| [`docs/`](docs/) | How the repository works: architecture, standards, onboarding, evaluation. |
| [`governance/`](governance/) | Security, compliance, review checklist, approved patterns—enterprise guardrails. |

---

## Contributing

We welcome PRs that improve clarity, examples, evaluations, or implementations—**without** breaking the shared layout. Start here:

- [`CONTRIBUTING.md`](CONTRIBUTING.md) — naming, registry updates, PR checklist.
- [`docs/onboarding.md`](docs/onboarding.md) — contributor walkthrough.
- [`governance/review-checklist.md`](governance/review-checklist.md) — what reviewers expect.

---

## License

This scaffold is released under the [MIT License](LICENSE). Replace or augment with your organization’s licensing policy if you fork internally.

---

## Optional future enhancements

- Schema-validated `agent.yaml` and registry entries in CI.
- Auto-generated catalog pages from `agents-index.yaml`.
- Shared tool manifests (OpenAPI/MCP) under `shared/tools/`.
- Golden-test runner wired to `examples/` and `tests/test-plan.md`.

The repository today stays **practical and documentation-first** so teams can adopt it immediately and harden over time.
