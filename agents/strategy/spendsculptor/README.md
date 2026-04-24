# SpendSculptor

SpendSculptor is the **data foundry** for procurement analytics: it **cleans**, **normalizes**, **maps taxonomy**, and **enriches** spend so strategy and control agents do not run on garbage.

## Why it matters

Bad taxonomy makes every dashboard lie. SpendSculptor focuses on **repeatable hygiene**—with **exceptions routed to stewards** and **lineage** that survives audits.

## Common inputs

- Messy AP exports (dirty descriptions, mixed languages)
- Multiple ERP vendor IDs for the same legal entity
- Commodity trees with version history

## Typical outputs

- Curated fact table: normalized supplier, site, commodity, UoM, currency
- Exception workbook: unmapped lines, conflicting rules, low-confidence matches
- Lineage notes: which rule version mapped a row and why

## Workflow in practice

Run **monthly close** cycles and **taxonomy upgrade** migrations. Feed **Spendscape**, **Spend Control Tower**, and **ICM** with consistent keys.

## Extension opportunities

- ML-assisted classification with **human-in-the-loop** approval
- Automated vendor dedupe suggestions with confidence scores
- Golden datasets in `shared/datasets/` for regression

## Differentiation

- **Spendscape** explains strategic implications of spend.
- **SpendSculptor** makes the **underlying facts trustworthy**.
