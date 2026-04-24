# Shared tools

## Purpose

Describe **tool contracts** (APIs, MCP servers, RPA hooks) that agents may call. This folder is documentation-first; actual SDKs may live elsewhere.

## What belongs here

- Tool manifests: purpose, inputs, outputs, auth model, rate limits, failure modes.
- Shared **idempotent** operations (e.g., “resolve supplier master ID”) used by multiple agents.

## What stays local

- Agent-specific orchestration (“call tool A then B with these joins”) belongs in that agent’s `workflows/` or implementation in `src/`.

## Safety

Document:

- Whether a tool is **read-only** or **write**.
- Required **human approval** gates for spend-affecting actions.

## Naming

Use clear, vendor-neutral names where possible; note vendor adapters in the tool description.
