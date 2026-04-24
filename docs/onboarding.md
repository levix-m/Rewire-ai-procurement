# Contributor onboarding

## Before you start

1. Read [overview.md](./overview.md) and [standards.md](./standards.md).
2. Identify the **domain** for your agent (`strategy`, `sourcing`, `negotiation`, `performance-management`, `value-preservation`).
3. Confirm the agent **does not already exist** under `agents/` or in [registry/agents-index.yaml](../registry/agents-index.yaml).

## Add a new agent

1. Copy `templates/agent-template/` to `agents/<domain>/<your-agent-folder>/`.
2. Replace placeholders in **all** files:
   - Update `README.md` with purpose, inputs, outputs, and workflows.
   - Fill `agent.yaml` with accurate metadata (see [registry/required-metadata.md](../registry/required-metadata.md)).
   - Customize `prompts/`, `workflows/`, `examples/`, `evals/`, and `tests/`.
3. Add a new entry to `registry/agents-index.yaml` with the same `id` and consistent `path`.
4. Open a PR using the checklist in [CONTRIBUTING.md](../CONTRIBUTING.md).

## Improve an existing agent

- Prefer **incremental PRs**: documentation clarity, better examples, stricter eval criteria, or test scenarios.
- If behavior changes materially, bump **`status` / `maturity`** only when your organization’s criteria are met.
- Keep **examples realistic** but non-sensitive; anonymize numbers and names.

## Work with shared assets

- If you introduce a reusable schema or prompt fragment, add it under `shared/` in the right subfolder and **link to it** from agent READMEs.
- Document **when to use** the shared asset in the shared README to avoid silent coupling.

## Evaluation expectations

Before promoting maturity:

- Review [evaluation-framework.md](./evaluation-framework.md).
- Ensure `evals/evaluation-criteria.md` matches how you actually judge quality.
- Extend `tests/test-plan.md` with regression cases when you fix defects.

## Getting help

- Tag maintainers listed in [CODEOWNERS](../CODEOWNERS) after you update it for your organization.
- For security-sensitive questions, read [governance/security.md](../governance/security.md) first.
