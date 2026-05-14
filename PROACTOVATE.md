# Proactovate Engineering Standards

Synced from `proactovate/standards`. Do not edit in this repo, changes will be overwritten.

## Code Conduct

- Make the minimal change needed. Do not refactor adjacent code without an explicit ask.
- When uncertain about scope or intent, ask before implementing.
- Match the existing style of the file being edited, even if it differs from conventions elsewhere.
- Comments explain why, not what. Do not restate the code.

## Git and Pull Requests

- One logical change per PR. Split unrelated work.
- PR titles use imperative mood ("Add X", not "Added X").
- PR descriptions cover the why, link the ticket if one exists, and flag anything reviewers might miss.
- Never force-push to shared branches.
- Never commit secrets, API keys, tokens, or `.env` files.

## Testing

- Add or update tests for any behavior change.
- Run the full suite locally before opening a PR.
- Do not skip, disable, or weaken existing tests to make a PR pass. If a test is genuinely wrong, fix it in a separate commit with explanation.

## AWS and Infrastructure

- Infrastructure is code. No console-only changes to production resources.
- Lambda functions stay small and single-purpose. Prefer Step Functions or SQS for orchestration over long-running Lambdas.
- DynamoDB: document access patterns in the repo, never query without a key or index.
- Use Secrets Manager or Parameter Store for credentials, never environment variables for sensitive values.

## Security

- HIPAA-covered repos are flagged in COMPANY.md. In those: no PHI in logs, error messages, or unencrypted storage.
- Sanitize and validate all input at the boundary.
- Never log credentials, tokens, or full request payloads.

## Communication

- Address team and client contacts with formal honorifics (Mr./Mrs.) in PR comments, commit messages, and documentation.
- Be direct. No filler, no apologies for normal disagreement.
- Never use em dashes in any written output.
- //test
