# 03 -- Data Integrity And Validation

## Purpose

Use this prompt to find places where bad, missing, duplicated, stale, or malicious data could corrupt the system or produce incorrect results.

## When To Use This Prompt

Use this when the system stores data, updates records, imports files, processes forms, handles payments, syncs with another service, or depends on workflow status.

## Copy/Paste Prompt

```text
You are reviewing data integrity and validation for an AI-assisted build.

Assume the user enters malformed, malicious, missing, duplicated, or unexpected data. Assume two users or jobs may update the same record at the same time. Assume third-party systems may send stale, partial, or repeated events.

Do not focus only on form validation. Review the full data path from input to storage to later use.

Look for:
- unclear data model assumptions
- missing required fields
- weak type and format validation
- server-side validation gaps
- duplicate submission risks
- race conditions
- concurrency issues
- partial update problems
- stale data problems
- missing database constraints
- bad default values
- incorrect date, time, timezone, or currency handling
- import and export risks
- data deletion and retention problems
- backup and recovery concerns

For each issue, explain what bad data could enter, how it could spread, what user-visible failure it could cause, and how to prevent or detect it.
```

## Expected Output Format

```text
Data Flow Summary
- ...

Integrity Findings
| Finding | Category | Severity | Bad Data Scenario | Evidence | Prevention | Detection |
| --- | --- | --- | --- | --- | --- | --- |

Database Or Storage Checks
- ...

Validation Rules Needed
- ...
```

## Follow-Up Prompts

- What database constraints should exist?
- What should be validated on the server even if the client already validates it?
- Where could duplicate submissions or repeated webhooks cause damage?
- Which records need audit history or recovery options?

## Red Flags To Look For

- Validation exists only in the UI.
- Important status changes are not transactional.
- Duplicate webhook events can create duplicate records or charges.
- There is no unique constraint for data that should be unique.
- Backups exist but restore has never been tested.

