# Pull request review checklist

Use this list before merging changes that affect agent behavior, metadata, or governance.

## Scope and structure

- [ ] Changes map cleanly to one domain (`strategy`, `sourcing`, etc.) unless a cross-cutting update is intentional.
- [ ] Agent folder matches **required layout** (see [docs/standards.md](../docs/standards.md)).
- [ ] No secrets, credentials, or customer-confidential content.

## Metadata and registry

- [ ] `agent.yaml` is valid YAML and complete for the schema your org uses.
- [ ] Matching entry in `registry/agents-index.yaml` updated (`id`, `path`, `category`, `status`, `maturity`, `owner`).
- [ ] `path` matches the actual folder (case-sensitive on some systems).

## Content quality

- [ ] README explains **purpose**, **inputs**, **outputs**, and **limitations**.
- [ ] Examples are realistic but **non-sensitive**.
- [ ] Workflows include **escalation** or **human review** where impact is high.

## Evaluation and tests

- [ ] `evals/evaluation-criteria.md` still reflects how quality is judged.
- [ ] `tests/test-plan.md` covers new scenarios for bug fixes or new edge cases.

## Risk

- [ ] Security implications reviewed for new tools or data access (see [security.md](./security.md)).
- [ ] Compliance sensitivities noted for regulated categories (see [compliance.md](./compliance.md)).

## Shared assets

- [ ] If adding to `shared/`, README explains reuse boundaries.
- [ ] Agents reference shared assets without creating circular ambiguity.

## Communication

- [ ] PR description states **user-visible impact** and **rollback** approach if deployed.
