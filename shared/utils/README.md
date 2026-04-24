# Shared utilities

## Purpose

Cross-cutting helpers: date and currency normalization, unit conversion, deterministic hashing for deduplication, redaction utilities, and small algorithms referenced by multiple agents.

## Language policy

This repository is **language-agnostic**. Utilities may be:

- Documented pseudocode,
- Implemented in your org’s standard language in `src/` subtrees later, or
- Linked as external packages **described** here.

## What belongs here

- Logic used by **three or more** agents or by both prompts and code paths.

## What stays local

- One-off ETL for a pilot category.
- Brand-specific formatting.

## Testing

If code is added, mirror test expectations in the owning package; keep agent `tests/test-plan.md` aligned for black-box behavior.
