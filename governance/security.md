# Security

## Threat model (starter)

Procurement agents may access spend data, supplier profiles, contracts, and employee identifiers. Treat the **documentation and examples** in this repository as if they could accidentally teach a model or engineer the wrong data-handling habits.

## Data classification

- Do not commit **restricted** or **secret** material. Use synthetic or public-domain-style examples.
- Redact names, account numbers, and site locations unless explicitly approved for training materials.

## Secrets and credentials

- No API keys, OAuth tokens, private keys, or connection strings in repo files.
- Use your organization’s secret manager in deployed environments.

## Tool use and side effects

Agents that can **create POs**, **send supplier communications**, or **modify contracts** must:

- Enforce **least privilege** credentials.
- Default to **dry-run** or **human-in-the-loop** approval where impact is irreversible.

## Prompt injection and untrusted content

When agents process **supplier-submitted** text (RFx responses, emails, invoices):

- Assume content may attempt **instruction injection**.
- Prefer structured parsers and allowlisted tool calls over free-form execution.

## Supply chain

- Pin dependencies when code is introduced.
- Scan for vulnerabilities per enterprise policy.

## Incident response

If sensitive data is committed:

1. Rotate affected credentials.
2. Purge history per Git hosting provider guidance.
3. Notify security and procurement leadership per your playbook.

## Review expectations

Security-sensitive changes should involve your **security** and **procurement operations** partners before production promotion.
