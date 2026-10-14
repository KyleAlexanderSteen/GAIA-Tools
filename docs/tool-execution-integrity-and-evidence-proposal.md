# Tool Execution Integrity and Evidence — Proposal

**Status:** Proposed; not approved or implemented.
**Canonical proposal:** https://github.com/KyleAlexanderSteen/GAIA-Documentation/blob/docs/alignment-attunement-self-improvement/GAIA-Documentation/GAIA-Universal-Principles-Integrity-Knowledge-and-Flourishing.md

## Candidate requirements

- Maintain an explicit registry of tool identity, capability, input/output contract, permission scope, risk class, and owner.
- Validate authorization at the execution boundary, not only in the planner or UI.
- Treat tool outputs as evidence with origin, timestamp, result status, and limitations—not as unquestionable truth.
- Distinguish planned, attempted, succeeded, failed, timed out, denied, and unverified actions.
- Preserve enough structured result metadata for audit and reproducibility without logging secrets or unnecessary personal data.
- Use idempotency, bounded retries, timeouts, and compensation/rollback where appropriate.
- Never report a tool action as completed if it was not executed or its result is unknown.
- Ensure denied actions cannot be retried through alternate tools to bypass the same policy.

## Tests to define

Permission matrix and denial tests; malformed/oversized inputs; timeout and partial failure; replay/idempotency; forged or stale outputs; audit redaction; and result-status honesty. Contracts and security policies must be approved before implementation.