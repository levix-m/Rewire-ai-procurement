# Sample input — Invoice to Contract Compliance

## Contract schedule (excerpt)

- SKU **LAB-TEMP-001**: **$28.50/hr** effective **2026-01-01** through **2026-12-31**
- Overtime multiplier **1.5x** only when PO line marked **OT-ALLOWED**

## Invoice lines (illustrated)

| Inv line | SKU | Qty | UOM | Unit | Ext |
|----------|-----|----:|-----|-----:|----:|
| 10 | LAB-TEMP-001 | 240 | HR | 29.75 | 7140 |
| 11 | LAB-TEMP-001 | 60 | HR | 43.12 | 2587 |

## PO context

- PO-7788 line 3 allows standard hours only; **no OT-ALLOWED** flag

## Tolerance

- Finance allows **$0.00** unit price variance for temp labor (strict)
