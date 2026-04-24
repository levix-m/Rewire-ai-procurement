# Shared schemas

## Purpose

Canonical **data shapes** for spend records, RFx artifacts, supplier scorecards, contract clauses, and invoice lines—so agents and tools agree on field names and units.

## What belongs here

- Versioned JSON Schema, YAML type definitions, or protobuf-style descriptions **without** customer data.
- Cross-agent enumerations (e.g., `maturity`, `status` values if extended beyond the registry).

## What stays local

- Mappings from a customer’s **legacy** column names to a canonical schema (often one-off).
- Experimental schemas used by a **single** pilot agent until stabilized.

## Versioning

When breaking changes are unavoidable:

1. Bump a version suffix in the filename or use a `v2/` subfolder.
2. Update dependent agents in the same change set or migration plan.

## CI (optional future)

Wire schema validation in continuous integration so `agent.yaml` and example payloads stay valid.
