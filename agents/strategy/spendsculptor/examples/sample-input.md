# Sample input — SpendSculptor

## Extract

AP lines from **SAP + legacy JDE** for Q1, merged by analytics team (anonymized).

## Sample dirty rows

| Line | Vendor text | Amount | UoM | Desc snippet |
|------|---------------|-------:|-----|--------------|
| 1 | ACME CO | 450 | EA | BEARING 6205-2RS |
| 2 | ACME COMPANY INC | 450 | ea | bearing 6205 2rs |
| 3 | UNKNOWN | 1200 | | misc supplies plant 7 |

## Taxonomy

Internal commodity tree **v2026.1** with MRO branch refinements.

## Policy

- Must retain **plant code** even if null in 4% of rows (flag, don’t drop)
