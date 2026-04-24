# Shared prompts

## Purpose

This folder holds **reusable prompt fragments** and **policy-safe boilerplate** that multiple procurement agents should share—so contributors do not fork slightly different versions across agents.

## What belongs here

- Universal guardrails (PII minimization, refusal patterns for legal advice, escalation language).
- Standard definitions (e.g., how “savings” is classified when your organization has a canonical typology).
- Reusable task scaffolds that are not tied to one category or supplier.

## What stays in an agent folder

- System prompts that encode **specific** decision logic for one agent.
- Examples that reveal **customer-specific** policies or thresholds.
- Prompts that only make sense with **one tool** or **one data layout**.

## How to use

1. Add a new fragment with a **clear name** (e.g. `savings-typology-guardrails.md`).
2. Document **which agents** should import or reference it in this README.
3. In agent `prompts/system.md`, reference the fragment explicitly (copy or include, depending on your runtime).

## Maintenance

Changes here may affect **many** agents. Require broader review per your governance process when editing shared guardrails.
