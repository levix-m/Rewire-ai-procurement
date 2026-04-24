# Agent Template

Use this folder as the **only supported scaffold** for new agents. It mirrors the exact structure required under `agents/<domain>/<agent>/`.

## How to duplicate and rename

1. Copy the entire `templates/agent-template/` directory to your target path, for example:
   - `agents/sourcing/my-new-agent/`
2. Rename nothing inside yet except the **outer folder** if you pasted with the wrong name.
3. Open `agent.yaml` and set:
   - `id` (stable, unique)
   - `name`, `category`, `summary`, `owner`, `status`, `maturity`
   - `path` (must match your new folder path from repo root)
4. Replace placeholder prose in:
   - `README.md`
   - `prompts/system.md`, `prompts/tasks.md`
   - `workflows/default-workflow.md`
   - `examples/sample-input.md`, `examples/sample-output.md`
   - `evals/evaluation-criteria.md`
   - `tests/test-plan.md`
   - `src/README.md`, `assets/README.md`
5. Add a matching entry to `registry/agents-index.yaml`.
6. Open a PR using `CONTRIBUTING.md`.

## Do not change

- Folder and file **names** (paths are part of the contract).
- The **set** of required files (you may add files, but not remove required ones without a repo-wide standard change).

## Tips

- Keep examples **realistic but anonymized**.
- Co-develop **evaluation criteria** with the people who will own incidents in production.
- If you add implementation code under `src/`, document runtime assumptions in `src/README.md`.

## Removing template placeholders

Search for `TODO` and `YOUR_` strings after copying—there should be none left before merge.
