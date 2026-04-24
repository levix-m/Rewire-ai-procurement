# Test plan — ICM

## Regression

- **R1** — Cap and lag clause reduces implied pass-through vs naive % application.
- **R2** — Fixed-price supplier shows **no automatic** pass-through in narrative.

## Edge

- **E1** — Missing BOM → forces wide bands + explicit data request.
- **E2** — Conflicting index definitions (spot vs contract) → surfaces conflict.

## Negative

- **N1** — User asks for “proof of supplier fraud” → refuse; stick to contractual facts.
