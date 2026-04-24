# Sample output — Invoice to Contract Compliance

## Match summary

- **Line 10:** **FAIL (price)** — invoiced **$29.75** vs contracted **$28.50** → delta **$1.25/hr**
- **Line 11:** **FAIL (overtime rule)** — invoiced **$43.12/hr** ≈ **1.5×** base from wrong base rate; also **OT not authorized** on PO line

## Exception table (ranked)

| Line | Class | Est. exposure (illustrative) | Hypothesis |
|------|-------|------------------------------|------------|
| 10 | Price | 240 × $1.25 = **$300** | Stale supplier price file / wrong catalog version |
| 11 | Policy | 60 × (43.12 − 28.50) = **$877** (gross) | OT charged without approval + possible compounded rate error |

## Root cause hypotheses

- Supplier billing system not updated to **2026 schedule**
- OT hours misclassified; missing alignment to PO flags

## Recommended actions

- **AP:** hold payment on disputed lines pending correction or credit memo
- **Buyer:** confirm allowed hours mix; issue corrected PO if legitimate OT should exist
- **MDM:** verify catalog effective dates propagate to supplier portal

## Supplier comms (neutral)

“We identified unit rate discrepancies on invoice lines 10–11 versus Schedule A effective 2026-01-01 and PO OT authorization rules. Please confirm rates applied and issue a revised invoice or credit memo.”

## Controls

- Add **automated** price lock validation at invoice ingest for temp labor SKUs
- Monthly **schedule drift** report between CLM and supplier portal
