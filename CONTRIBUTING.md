# Contributing to Procurement Agents

Thank you for helping grow a **structured**, **governed** library of procurement agents. Consistency matters more than speed: the same layout in every folder keeps automation, search, and onboarding predictable.

## Quick start: add a new agent

1. **Copy the template**  
   Duplicate `templates/agent-template/` to `agents/<domain>/<agent-folder>/`.

2. **Choose the domain**  
   Use one of: `strategy`, `sourcing`, `negotiation`, `performance-management`, `value-preservation` (see [registry/categories.yaml](registry/categories.yaml)).

3. **Name the folder (kebab-case)**  
   Lowercase, hyphen-separated, no spaces. Examples: `invoice-to-contract-compliance`, `icm-input-cost-monitor`.

4. **Replace every placeholder**  
   Update README, YAML, prompts, workflows, examples, evals, tests, and the `src/` / `assets/` README stubs.

5. **Register the agent**  
   Add an entry to [registry/agents-index.yaml](registry/agents-index.yaml) with the same `id` as in `agent.yaml` and the correct `path`.

6. **Open a pull request**  
   Use the checklist below and request review from CODEOWNERS.

## Folder naming conventions

| Rule | Good | Avoid |
|------|------|--------|
| Lowercase kebab-case | `supplier-performance-cockpit` | `SupplierPerformanceCockpit` |
| Stable over clever | `rfx-creator` | `rfx-creator-v2-temp` |
| Match registry `path` exactly | `agents/sourcing/s4g` | Drift between YAML and disk |

Display names and branding (e.g. **S4G**) live in `name` fields and README titles, not necessarily in folder names.

## Minimum required files

Each agent **must** include:

- `README.md`
- `agent.yaml`
- `prompts/system.md`, `prompts/tasks.md`
- `workflows/default-workflow.md`
- `examples/sample-input.md`, `examples/sample-output.md`
- `evals/evaluation-criteria.md`
- `tests/test-plan.md`
- `src/README.md`, `assets/README.md`

## Evolving content vs structure

- **Starter content is meant to be replaced** as your organization’s playbooks evolve.
- **Do not rename or remove required paths** without a deliberate migration (registry, links, and CI may depend on them).
- Major rewrites should update **evaluation criteria** and **tests** in the same PR when behavior changes.

## Updating `registry/agents-index.yaml`

For every agent change that affects discoverability or ownership:

- Keep **`id`** identical to `agent.yaml`.
- Update **`status`** and **`maturity`** when promotion or deprecation happens.
- Ensure **`path`** matches the folder on disk.
- Refresh **`summary`**, **`primary_inputs`**, **`primary_outputs`**, **`key_workflows`**, and **`dependencies`** when scope changes.

If you split an agent, **deprecate** the old `id` in documentation and add the new entry in the same PR when possible.

## Pull request checklist

- [ ] Required layout present and populated (no empty stubs).
- [ ] `agent.yaml` and `registry/agents-index.yaml` aligned.
- [ ] Examples anonymized; no secrets or customer-confidential data.
- [ ] `evals/evaluation-criteria.md` and `tests/test-plan.md` reflect the change.
- [ ] Links in READMEs resolve (relative paths).
- [ ] Governance-sensitive changes referenced in PR description (tools, PII, regulated categories).

## Documentation expectations

- **README**: purpose, users, inputs, outputs, workflow summary, limitations, extension ideas.
- **prompts**: procurement-specific, with guardrails appropriate to risk.
- **workflows**: steps, roles, escalation, and human gates where needed.

## Evaluation expectations

- Define **5–8** measurable criteria in `evals/evaluation-criteria.md`.
- Maintain **golden** or representative examples in `examples/`.
- Add **regression** and **edge-case** scenarios to `tests/test-plan.md` when fixing defects.

## Test coverage expectations

This repo is **language-agnostic**. “Tests” may start as documented plans. As code lands in `src/`:

- Mirror critical behaviors with automated tests in your chosen stack.
- Keep the **documented** test plan updated—automation should not drift from stated intent.

## Shared assets

If you introduce something reusable for many agents, add it under `shared/<area>/` and document when to use it. Link from agent READMEs rather than duplicating large fragments.

## Code of conduct and review

Follow your organization’s code of conduct. Reviewers use [governance/review-checklist.md](governance/review-checklist.md) alongside this guide.

## Questions

Open a discussion with maintainers (update contact paths in [CODEOWNERS](CODEOWNERS) for your enterprise).
