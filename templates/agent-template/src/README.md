# Source code — template

## Intent

Implementation code for this agent (services, batch jobs, notebooks-as-production, etc.) should live here when you outgrow prompt-only prototypes.

## Guidelines

- Keep orchestration **thin**; business rules should be testable.
- Document how to configure environments without committing secrets.
- Prefer explicit interfaces for data inputs/outputs (see `shared/schemas/`).

## Suggested layout (optional)

```text
src/
├── README.md          # You are here
├── connectors/        # ERP, CLM, data lake readers
├── logic/             # Deterministic transforms and validators
└── runtime/           # Agent server or CLI entrypoints
```

Replace this file with project-specific instructions when code exists.
