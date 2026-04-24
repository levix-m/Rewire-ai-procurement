# Default workflow — template

## Goal

Produce a reliable, reviewable outcome for a routine procurement scenario using this agent.

## Preconditions

- Required datasets are available (list them explicitly for your agent).
- Owners and approvers are identified for high-impact recommendations.

## Steps

1. **Intake** — Confirm scope, time horizon, geography, and category definitions.
2. **Validate inputs** — Check freshness, completeness, and known data defects.
3. **Analyze** — Apply the agent’s core logic (prompt, rules, or code).
4. **Sense-check** — Compare outputs to benchmarks or historical patterns.
5. **Package** — Render results in the agreed format (brief, dashboard export, etc.).
6. **Review gate** — Route through human approval if required by policy.
7. **Publish & learn** — Log decisions, capture feedback, update evals if needed.

## Escalation

- **Data missing** → pause and request stewardship fixes rather than silent guesses.
- **High financial exposure** → involve Finance and Category Director.
- **Legal interpretation** → route to Legal, not the model’s improvisation.

Replace steps with domain-specific detail when instantiating the template.
