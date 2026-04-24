# Sample output — SpendSculptor

## Dataset health

- **98.2%** rows mapped to `supplier_id` (MDM confirmed)
- **1.1%** candidate alias merges pending approval (ACME CO / ACME COMPANY INC)
- **0.7%** unclassified MRO descriptions → steward queue Q_MRO_014

## Transformations applied

- Case normalization for UoM; standardized **EA**
- Rule pack `mro_bearings_v3` matched tokens `6205`, `2RS` → commodity `MRO.BEARINGS.BALL`
- `UNKNOWN` vendor routed to **site-level T&E card spillover** hypothesis (low confidence)

## Exception playbook

| Code | Meaning | Owner |
|------|---------|-------|
| Q_MRO_014 | Weak descriptions | Plant buyers |
| A_ALIAS_009 | Alias merge suggestion | MDM team |

## Lineage

- Taxonomy **v2026.1**; ruleset hash `sha256:…` (placeholder)
- FX: corporate month-end table **2026-Q1**

## Reconciliation

- Total spend delta vs raw: **+0.03%** (explained by duplicate line collapse in test env)
