# Architecture

## Conceptual model

Each **agent** is a bounded capability aligned to a procurement workflow domain (strategy, sourcing, negotiation, performance management, value preservation). Agents are **not** monolithic “procurement copilots”; they are composable units that can be orchestrated by a platform or used standalone.

```
Contributors → templates/agent-template → agents/<domain>/<agent>/
                              ↓
                    registry/agents-index.yaml (discoverability)
                              ↓
              shared/ (reuse)     governance/ (rules of the road)
```

## Folder responsibilities

### `agents/`

- **Domain folders** (`strategy`, `sourcing`, etc.) group agents the way procurement organizations think about work.
- **Agent folders** are kebab-case and stable; renaming is a breaking change for links and registry paths.

### `templates/agent-template/`

- The **only** sanctioned way to scaffold a new agent.
- Keeps `README.md`, `agent.yaml`, prompts, workflows, examples, evals, tests, `src/`, and `assets/` aligned.

### `registry/`

- **`agents-index.yaml`**: machine- and human-friendly catalog (ids, maturity, owners, paths).
- **`categories.yaml`**: controlled vocabulary for domains.
- **`required-metadata.md`**: schema expectations for index entries and `agent.yaml`.
- **`maturity-model.md`**: definitions for lifecycle stages.

### `shared/`

- **Prompt fragments**, **JSON/YAML schemas**, **tool descriptors**, **utilities**, and **reference datasets** that multiple agents should reuse.
- Agent folders stay **self-contained** for anything specific to one use case or one company’s policy pack.

### `docs/`

- Narrative documentation: standards, onboarding, evaluation philosophy.

### `governance/`

- Enterprise-oriented guardrails: security, compliance, review checklist, approved patterns.

## Metadata flow

1. Author fills **`agent.yaml`** inside the agent folder (source of truth for that agent).
2. Author adds or updates the matching entry in **`registry/agents-index.yaml`**.
3. Reviewers check **parity** between the two and the **folder path**.

Keeping registry and `agent.yaml` in sync enables generated catalogs, internal portals, and CI checks later without restructuring content.

## Implementation styles (supported)

| Style | What lives in repo | Notes |
|-------|-------------------|--------|
| Prompt-first | `prompts/`, `workflows/` | Ideal for LLM-only or low-code orchestration. |
| Workflow-first | `workflows/`, `examples/` | BPMN or markdown runbooks can be referenced from `assets/`. |
| Code-based | `src/` | Language-agnostic; add runtimes and packages as needed. |

The **documentation shell** does not change when implementation style changes.

## Extension points (future-friendly)

- **Schema validation** of `agent.yaml` and the registry via CI.
- **Generated README tables** from `agents-index.yaml`.
- **Shared tool registry** under `shared/tools/` with formal OpenAPI or MCP manifests.

These are optional; the current layout stays valid without them.
