# Default workflow — SpendSculptor

## Goal

Publish a **curated spend slice** with documented transformations for a reporting cycle.

## Steps

1. **Ingest** raw files; checksum and snapshot “as received.”
2. **Profile** columns: null rates, top tokens, language mix, currency mix.
3. **Normalize** suppliers via MDM keys; stage alias suggestions separately.
4. **Classify** commodities using rule packs + ML assist (if enabled).
5. **Validate** totals vs source (hash checks, aggregate reconciliation).
6. **Exception routing** — queues by steward team with SLAs.
7. **Publish** curated dataset + dictionary; version the taxonomy reference.
8. **Notify downstream** — Spendscape/Control Tower consumers of breaking changes.

## Escalation

Unexplained **aggregate drift** >1% → halt publish until root-caused.
