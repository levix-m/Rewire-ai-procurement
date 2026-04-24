# Approved patterns

## Purpose

Lightweight pattern library for building **consistent**, **reviewable** procurement agents. Adapt names to your tech stack; keep the **ideas**.

## Pattern: Assumption ledger

**When**: Inputs are incomplete (common with spend files).

**How**: The agent emits an explicit table of assumptions (e.g., default payment terms, FX source) separate from recommendations.

**Why**: Auditors and peers can reconcile outputs later.

## Pattern: Confidence and evidence tags

**When**: Recommendations affect money or suppliers.

**How**: Tag each recommendation with `high | medium | low` confidence and point to **evidence** (dataset slice, clause ID, KPI trend).

**Why**: Reduces blind trust in LLM prose.

## Pattern: Human gate for write actions

**When**: Tools can email suppliers, publish RFxs, or post pricing.

**How**: Two-step flow: draft → approval record → execute.

**Why**: Prevents automation errors from becoming contractual reality.

## Pattern: Golden examples in `examples/`

**When**: Any agent promoted beyond `experimental`.

**How**: Maintain paired `sample-input.md` / `sample-output.md` that the team agrees is “good enough.”

**Why**: Stable regression anchors.

## Pattern: Separation of policy and reasoning

**When**: Organizational rules change often.

**How**: Keep numeric thresholds and policy excerpts in **versioned** documents or tools, not buried only in long system prompts.

**Why**: Faster, safer updates.

## Pattern: Supplier fairness narrative

**When**: Performance or negotiation agents discuss suppliers.

**How**: Distinguish **data quality issues** from **performance issues**; avoid subjective labels without criteria.

**Why**: Reduces reputational and legal risk.

## Anti-patterns

- **Opaque scoring**: black-box scores without criteria or weights.
- **Unbounded web browsing** for supplier diligence without caching and attribution.
- **Mixing** internal strategy content with supplier-facing text without a clear boundary.

## Adding patterns

Propose new patterns via PR with: problem, solution shape, and an example agent reference.
