# Maturity model

## Why this exists

`maturity` and `status` fields help contributors and executives understand **how ready** an agent is for broad use—without hiding that some agents are exploratory.

## Status (`status`)

| Value | Meaning |
|-------|---------|
| `planned` | Documented intent; implementation not started or not merged. |
| `experimental` | Active development; outputs may be wrong or unstable. |
| `beta` | Usable with known limitations; feedback loop in place. |
| `production` | Approved for defined scopes; owners on the hook for incidents. |
| `deprecated` | Being phased out; migration path documented. |

## Maturity (`maturity`)

| Level | Name | Typical evidence |
|-------|------|------------------|
| 0 | Concept | README and metadata only; examples illustrative. |
| 1 | Scaffold | Prompts/workflows drafted; no production data path. |
| 2 | Pilot | Running on anonymized or limited prod slices; evals exercised. |
| 3 | Scaled | Multiple teams or categories; regression tests maintained. |
| 4 | Industrialized | SLOs, monitoring, ownership rotation, security/compliance sign-off. |

## Promotion rules (organization-specific)

Your enterprise should define **who can promote** an agent from `experimental` → `beta` → `production`. Minimum suggested gates:

- Documented evaluation results against `evals/evaluation-criteria.md`
- Security review for tools and data access
- Rollback plan for orchestration changes

## Deprecation

When deprecating:

1. Set `status: deprecated` in `agent.yaml` and the registry.
2. Add a **sunset date** and **replacement agent id** in the README.
3. Archive or redirect examples that might confuse users.
