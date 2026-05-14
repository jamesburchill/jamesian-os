# 01 -- Basic Safety Review

## Purpose

Use this prompt to get a first-pass safety review of an AI-assisted app, website, automation, prototype, script, or internal tool. The goal is to identify obvious risks before going deeper.

## When To Use This Prompt

Use this early in the review, after you can describe what the system does, who uses it, what data it touches, and where it runs.

## Copy/Paste Prompt

```text
You are reviewing an AI-assisted build. Do not reassure me unless the evidence supports it.

Assume the system works in the happy path, but may fail under real use.

Review the app description, screenshots, code, configuration, logs, schema, dependencies, and deployment notes I provide. If evidence is missing, say so clearly.

Look for:
- unclear assumptions
- unclear purpose or user flow
- user input risks
- authentication concerns
- authorization concerns
- secrets handling issues
- privacy risks
- missing validation
- missing error handling
- missing logging or observability
- backup and recovery gaps
- operational support risks
- maintainability risks

Do not give a generic answer. Tie every concern to the evidence I provided, or mark it as an assumption that needs verification.

For each issue, classify it using one of these categories:
- Cosmetic
- Usability Risk
- Reliability Risk
- Security Risk
- Data Integrity Risk
- Privacy Risk
- Financial Risk
- Legal/Compliance Risk
- Operational Risk
- Catastrophic Failure Risk

Use one severity:
- Low
- Medium
- High
- Critical

Start by listing the assumptions you are making. Then identify the highest-risk unknowns.
```

## Expected Output Format

```text
Assumptions
- ...

Missing Evidence
- ...

Top Risks
| Risk | Category | Severity | Evidence | Why It Matters | Suggested Fix |
| --- | --- | --- | --- | --- | --- |

Quick Wins
- ...

Do Not Ignore
- ...
```

## Follow-Up Prompts

- Which of these risks should block launch?
- Which claims in your review are based on missing evidence?
- What should I inspect manually before trusting this answer?
- Rewrite the top risks as an issue log with owner, severity, and verification steps.

## Red Flags To Look For

- The review says "looks good" without evidence.
- Authentication or authorization is not mentioned.
- The answer ignores data loss, recovery, or operational support.
- The answer treats a prototype as production-ready because it runs.
- The answer does not separate confirmed findings from assumptions.

