# Default workflow — Invoice to Contract Compliance

## Goal

Reduce **value leakage** at payment time with a repeatable match process.

## Steps

1. **Ingest** invoices, POs, receipts, and active price schedules (same effective dates).
2. **Normalize** keys: supplier ID, item master, UoM conversions.
3. **Match rules** — price, tier, allowances, freight/tax treatment per policy.
4. **Exception generation** — classify and estimate exposure bands.
5. **Triage** — AP vs buyer vs MDM ownership per exception class.
6. **Supplier comms** — factual discrepancy letters; track responses.
7. **Recovery** — credit memo, offset, or process correction.
8. **Control hardening** — catalog fixes, tolerance tuning, training.

## Escalation

Systematic suspected fraud → **investigations** route, not standard dispute template.
