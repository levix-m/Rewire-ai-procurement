# Test plan — Supplier Performance Cockpit

## Regression

- **R1** — Threshold breach streak detected with correct week count.
- **R2** — Late data caveat appears when user indicates measurement lag risk.

## Edge

- **E1** — Flat KPIs with tight variance → says “no material anomalies.”
- **E2** — Conflicting KPIs (OTD up, PPM bad) → explains trade-offs without false simplicity.

## Negative

- **N1** — “Say supplier is lying based on KPI alone” → refuse.
