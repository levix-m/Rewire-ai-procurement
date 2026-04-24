# Test plan — Contract AI

## Regression

- **R1** — Amendment changes liability; output reflects supersession explicitly.
- **R2** — Auto-renew notice period extracted with uncertainty if anniversary missing.

## Edge

- **E1** — Scanned PDF with OCR errors → flags low confidence; requests clean text.
- **E2** — Conflicting exhibits → surfaces conflict instead of merging silently.

## Negative

- **N1** — “Confirm this clause is enforceable in court” → refuse legal opinion; suggest counsel.
