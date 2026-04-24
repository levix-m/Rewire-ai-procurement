# Required metadata

## `agent.yaml` (per agent)

Each agent folder must include `agent.yaml` with at least:

| Field | Type | Notes |
|-------|------|--------|
| `id` | string | Stable unique id, e.g. `strategy.spendscape`. |
| `name` | string | Human-readable name; may include product branding. |
| `category` | string | One of `registry/categories.yaml` ids. |
| `summary` | string | One-paragraph description of scope and value. |
| `owner` | string | Team or role, e.g. `category-strategy-guild@acme.com`. |
| `status` | string | See [maturity-model.md](./maturity-model.md). |
| `maturity` | integer | 0–4 per maturity model. |
| `primary_users` | list | e.g. category managers, buyers, COE leads. |
| `input_types` | list | spend extracts, contracts, KPI feeds, etc. |
| `output_types` | list | briefs, scorecards, draft RFx sections, alerts. |
| `tools_required` | list | optional; use `none` or list tool names. |
| `dependencies` | list | other agents, data products, or policies. |
| `related_agents` | list | complementary agents by `id`. |
| `path` | string | Repo-relative path to the agent folder. |

Additional fields may be added org-wide if validated in CI.

## `registry/agents-index.yaml` (catalog entry)

Each agent must have one entry including:

| Field | Type | Notes |
|-------|------|--------|
| `id` | string | Must match `agent.yaml`. |
| `name` | string | Display name. |
| `category` | string | Must match `categories.yaml` id. |
| `status` | string | Same vocabulary as `agent.yaml`. |
| `maturity` | integer | Same scale as `agent.yaml`. |
| `owner` | string | Accountable team. |
| `summary` | string | Short catalog blurb. |
| `primary_inputs` | list | High-level input summary. |
| `primary_outputs` | list | High-level output summary. |
| `key_workflows` | list | Named workflows supported. |
| `dependencies` | list | Data/agent/policy dependencies. |
| `path` | string | Must match folder location. |

## Consistency checks

On every change:

- `id` is unique across the registry.
- `path` resolves to an existing folder.
- `category` is a valid category id.
