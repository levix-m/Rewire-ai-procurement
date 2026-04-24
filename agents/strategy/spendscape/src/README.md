# Source code — Spendscape

## Intended implementation

- Connectors to the **enterprise spend warehouse** (read-only) with parameterized slices
- Deterministic aggregations: concentration, tail PO stats, contract coverage joins
- Optional export to **slide generation** templates

## Notes

Keep heavy lifting in SQL/ELT where possible; use LLM layers for **narrative** and **opportunity phrasing**, not for recomputing totals.
