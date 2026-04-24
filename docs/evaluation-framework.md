# Evaluation framework

## Purpose

Procurement agents influence spend decisions, supplier relationships, and compliance posture. Evaluations must be **repeatable**, **documented**, and **proportionate** to risk.

This framework aligns agent-level `evals/evaluation-criteria.md` and `tests/test-plan.md` with a common philosophy.

## Dimensions

### 1. Correctness and grounding

- Outputs should reflect **stated inputs** and **explicitly labeled assumptions** when data is missing.
- Prefer **citations to internal artifacts** (policy doc IDs, contract clauses, RFx sections) when the deployment supports it.

### 2. Procurement usefulness

- Recommendations should be **actionable** for a category manager or buyer (clear next step, owner, timeframe).
- Avoid generic advice that could apply to any industry without tailoring hooks.

### 3. Consistency

- Similar inputs in similar contexts should yield **stable** conclusions; note intentional variance (e.g. stochastic models) in the README.

### 4. Risk and compliance awareness

- Flag **regulatory**, **trade**, or **contractual** sensitivities when relevant.
- Never fabricate legal interpretations; surface **escalation** paths.

### 5. Fairness and supplier impact

- Language should be **professional** and **non-discriminatory**.
- Performance narratives should distinguish **data gaps** from **supplier failure modes**.

### 6. Safety and data handling

- No PII or secrets in examples or logs referenced by tests.
- Red-team prompts for **prompt injection** and **unauthorized tool use** where tools exist.

### 7. Operability

- Outputs should be easy to **import** into downstream systems (tables, fields, units, currencies).
- Note required **master data** quality for the agent to function.

## Scoring (suggested)

Use a simple rubric in each agent’s evaluation doc:

| Score | Meaning |
|-------|---------|
| 0 | Unacceptable; blocks release |
| 1 | Major gaps; needs redesign |
| 2 | Acceptable with documented limitations |
| 3 | Strong; meets stated scope |

Track scores over time for the same **golden** examples in `examples/`.

## Golden sets

Maintain a small set of **golden inputs** (in `examples/` or anonymized fixtures) and expected **shape** of outputs:

- Exact text match is often unrealistic; define **structural** and **semantic** checks instead.

## Regression testing

Every defect fixed in production should add:

- A **test scenario** in `tests/test-plan.md`
- Optionally an **automated** check later without removing the documented scenario

## Roles

- **Agent owner**: ensures eval criteria stay current.
- **Peer reviewer**: runs spot checks against criteria before merge.
- **Risk/compliance**: consult for high-maturity promotion or regulated categories.

## Related documents

- [registry/maturity-model.md](../registry/maturity-model.md)
- [governance/review-checklist.md](../governance/review-checklist.md)
