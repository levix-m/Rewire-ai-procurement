# Standards

## Naming

- **Agent folder names**: `kebab-case`, lowercase, no spaces (e.g. `invoice-to-contract-compliance`).
- **Agent `id` in metadata**: stable identifier; prefer `domain.short-name` (e.g. `strategy.spendscape`). Do not rename casually.
- **Display `name`**: human-readable; may include branding (e.g. **S4G**).

## Required agent layout

Every agent under `agents/` must include:

- `README.md`
- `agent.yaml`
- `prompts/system.md`, `prompts/tasks.md`
- `workflows/default-workflow.md`
- `examples/sample-input.md`, `examples/sample-output.md`
- `evals/evaluation-criteria.md`
- `tests/test-plan.md`
- `src/README.md`, `assets/README.md`

Files may be **rewritten** over time; **paths must remain**.

## Documentation tone

- Prefer **procurement-native language**: category, supplier, RFx, contract, PO, invoice, SLA, savings, compliance.
- State **assumptions** (data availability, geography, regulated vs non-regulated spend) explicitly.
- Separate **example content** from **policy**: examples illustrate patterns; they are not legal advice.

## Metadata parity

`agent.yaml` and `registry/agents-index.yaml` must agree on:

- `id`, `name`, `category`, `status`, `maturity`, `owner`, `path`

Summaries may be shorter in the registry but must not contradict the agent README.

## Maturity and status

Use the definitions in [registry/maturity-model.md](../registry/maturity-model.md). Do not mark an agent as `production` without documented evaluation results and owner sign-off in your organization’s process.

## Shared vs local

| Put in `shared/` | Keep in the agent folder |
|------------------|---------------------------|
| Generic prompt clauses (safety, PII handling patterns) | Use-case-specific system behavior |
| Canonical taxonomy or schema for spend classes | Customer-specific mappings |
| Reusable tool contracts | Agent-specific tool wiring |
| Anonymized benchmark datasets | Customer data or exports |

## Version control hygiene

- No secrets, credentials, or customer data in the repo.
- Large binary assets: prefer links and descriptions in `assets/README.md`; host binaries per your org policy.

## Pull requests

Follow [CONTRIBUTING.md](../CONTRIBUTING.md) and [governance/review-checklist.md](../governance/review-checklist.md).
