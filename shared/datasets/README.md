# Shared datasets

## Purpose

**Reference, anonymized, or synthetic** datasets that help contributors test agents consistently—without using real supplier or employee data.

## What belongs here

- Small CSV/JSON fixtures that illustrate **shape** and **edge cases** (multi-currency, split POs, partial receipts).
- Data dictionaries describing columns and acceptable ranges.

## What never belongs here

- Production exports,
- Personal data,
- Confidential contract text.

## Provenance

For each dataset, document:

- **Origin** (synthetic vs anonymized),
- **Last updated** date,
- **License** for use inside your organization.

## Agent linkage

Agents should reference datasets from their `tests/test-plan.md` or `examples/` by **name**, not by embedding large tables in prompts.
