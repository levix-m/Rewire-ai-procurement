# Compliance

## Purpose

Starter guidance for organizations deploying procurement agents under **trade compliance**, **privacy**, **labor and ethics**, and **financial controls**.

## Not legal advice

These documents support **engineering and process design**. Legal and compliance teams must approve interpretations for your jurisdictions and industries.

## Common procurement compliance themes

### Competition and fair dealing

- Avoid agent outputs that could enable **bid rigging**, **discriminatory** supplier treatment without objective criteria, or **anticompetitive** signaling.
- Document **objective** scoring rules used in sourcing recommendations.

### Trade and sanctions

- If agents recommend suppliers or routes, ensure **sanctions screening** and **export control** checks are modeled as explicit gates—not implicit assumptions.

### Privacy

- Minimize personal data in prompts and logs.
- Honor **retention** schedules and **subject rights** processes where HR or contingent worker data appears in spend workflows.

### Records management

- Outputs that affect financial reporting or audit trails should be **versioned** and **attributable** (who ran the agent, when, on what data snapshot).

### Anti-bribery and gifts

- Agents that surface “relationship” insights should not normalize **improper inducements**; align to your gifts and entertainment policy.

## Documentation obligations

For regulated contexts, maintain:

- **Decision logs** for material recommendations.
- **Model and prompt change history** mapped to approvals.

## Supplier-facing outputs

Ensure communications drafted or edited by agents use **approved templates** and **disclaimers** where required.

## Escalation

Define **hard stops** (legal review, compliance review, category director approval) in workflows for high-risk categories (e.g., critical single-source, government sales).
