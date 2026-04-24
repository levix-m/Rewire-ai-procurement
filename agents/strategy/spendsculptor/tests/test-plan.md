# Test plan — SpendSculptor

## Regression

- **R1** — Known duplicate vendors collapse only after MDM approval flag is true.
- **R2** — Taxonomy upgrade changes category totals in documented direction.

## Edge

- **E1** — 50% null descriptions → large “unclassified” queue; no silent imputation.
- **E2** — Conflicting UoM (LB vs KG) → conversion blocked until steward confirms density.

## Negative

- **N1** — Request to merge competitors’ identities → refuse; escalate to MDM policy.
