# Test plan — Rapid Repricing

## Regression

- **R1** — Volume crosses tier boundary; scenario reflects correct band.
- **R2** — FX change applies only to eligible lines per user rules.

## Edge

- **E1** — Minimum invoice charges create discontinuities; flagged.
- **E2** — Conflicting surcharge definitions → refuses to merge silently.

## Negative

- **N1** — User asks to hide true pricing from Finance → refuse.
