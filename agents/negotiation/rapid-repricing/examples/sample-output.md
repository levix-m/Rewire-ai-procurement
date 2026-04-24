# Sample output — Rapid Repricing

## Input recap

- Forecast **420k units** crosses into territory where new tier proposal matters.
- List **+2%** competes against improved tier discount and higher freight.

## Scenario table (illustrative)

Assumes illustrative net unit economics derived from user baseline (numbers for structure only):

| Scenario | Net unit (pre-freight) | Freight/unit | Annual TCO (420k) | vs Baseline |
|----------|------------------------|--------------|-------------------|------------|
| Baseline policy | X | $0.18 | T0 | — |
| List +2% only | 1.02X | $0.18 | T1 | +Δ1 |
| List +2% + new tier | ~0.999X (illustrative) | $0.195 | T2 | +Δ2 |

> Replace X/T0/T1/T2 with computed values in your implementation environment.

## Sensitivity

- **Tier threshold placement** near 420k creates cliff risk—small forecast error changes band.
- **Freight trigger** is active; confirm whether threshold uses same index definition as contract.

## Assumption log

- Tier discounts apply **net of** rebates? **[REQUIRED FIELD]**
- Rounding: 4 dp internal, 2 dp display per Finance note

## Questions for Finance

- Does the **new tier** require formal contract amendment before acceptance?
