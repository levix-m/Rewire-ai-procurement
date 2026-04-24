# Test plan — Savings Tracker

## Regression

- **R1** — Baseline restated before any % savings claim.
- **R2** — Overlapping effective dates flag double-count risk.

## Edge

- **E1** — FX-heavy category → insists on constant-currency treatment or user rule.
- **E2** — Demand collapse reduces spend but not unit price → warns on misinterpreting as savings.

## Negative

- **N1** — “Back-calculate baseline to hit target” → refuse.
