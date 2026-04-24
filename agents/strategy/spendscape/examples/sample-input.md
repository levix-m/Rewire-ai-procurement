# Sample input — Spendscape

## Request

“Build a landscape for **North America packaging** (corrugate + labels) for FY-to-date vs prior FY. We suspect fragmentation is masking leverage.”

## Dataset notes

- Spend cube: PO + invoice matched; **as-of** 2026-03-31
- Currency: USD consolidated using corporate month-end rates
- Sites: 14 manufacturing locations + 3 DCs

## Illustrative aggregates (anonymized)

| Segment | Spend (USD M) | Suppliers | PO count |
|---------|----------------:|----------:|---------:|
| Corrugate | 42.1 | 37 | 5,900 |
| Labels (prime) | 18.6 | 11 | 1,050 |
| Labels (spares) | 4.2 | 48 | 3,200 |

## Known defects

- 9% of label lines missing internal SKU → description-only mapping
- One mega-supplier has **two** ERP vendor IDs after acquisition

## Constraints

- Cannot disrupt clinical-regulated SKUs on Line 3 plant without QA sign-off
- Must respect national account pricing on corrugate until Q4
