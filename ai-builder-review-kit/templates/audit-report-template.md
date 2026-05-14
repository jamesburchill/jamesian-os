# Audit Report Template

Use this template to summarize the review in plain language. Keep claims tied to evidence. Mark unknowns clearly.

## System Reviewed

- Name:
- Builder or owner:
- Review date:
- Reviewer:
- Intended users:
- Intended launch stage:
- Repository, URL, or environment reviewed:

## Executive Summary

Write a short summary of what was reviewed, the overall confidence level, and the recommended decision.

Recommended decision:

- [ ] Safe to continue experimenting
- [ ] Safe for private/internal use only
- [ ] Needs fixes before beta
- [ ] Needs expert review before launch
- [ ] Do not launch in current form

## Scope

Reviewed:

- [ ] App description
- [ ] Screenshots or demo
- [ ] Source code
- [ ] Configuration
- [ ] Environment variable list with secret values removed
- [ ] Database schema
- [ ] Logs or error reports
- [ ] Deployment notes
- [ ] Dependencies
- [ ] Backup and recovery notes
- [ ] Other:

Not reviewed:

- ...

## Key Assumptions

- ...

## Missing Evidence

- ...

## Top Risks

| Risk | Category | Severity | Evidence | Why It Matters | Recommended Fix |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |

## Production-Readiness Score

Total score: `__ / 100`

Lowest-scoring areas:

- ...

## Launch Blockers

- ...

## Recommended Fix Plan

| Priority | Fix | Risk Reduced | Owner | Verification |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |

## Residual Risk

Describe what risk remains after the recommended fixes, and whether that risk is acceptable for the intended launch stage.

## Final Recommendation

Choose one:

- [ ] Safe to continue experimenting
- [ ] Safe for private/internal use only
- [ ] Needs fixes before beta
- [ ] Needs expert review before launch
- [ ] Do not launch in current form

Reason:

...

