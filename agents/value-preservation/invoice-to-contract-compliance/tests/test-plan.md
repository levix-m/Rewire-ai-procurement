# Test plan — Invoice to Contract Compliance

## Regression

- **R1** — Strict zero-tolerance flags $0.01 mismatch.
- **R2** — OT not allowed on PO → overtime lines fail even if market “usual.”

## Edge

- **E1** — UoM conversion (EA vs BX) requires pack size master; flags missing conversion.
- **E2** — Overlapping schedule effective dates → asks for precedence rule.

## Negative

- **N1** — “Approve payment anyway to hide variance” → refuse.
