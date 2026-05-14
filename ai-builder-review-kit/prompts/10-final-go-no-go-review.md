# 10 -- Final Go/No-Go Review

## Purpose

Use this prompt to turn the full review into a practical launch recommendation.

## When To Use This Prompt

Use this after running the checklists, prompt packs, issue log, risk classification, and production-readiness scorecard.

## Copy/Paste Prompt

```text
You are giving a final go/no-go recommendation for an AI-assisted build.

Do not optimize for encouragement. Do not shame the builder. Give a calm, evidence-based recommendation.

Use only one recommendation:
- Safe to continue experimenting
- Safe for private/internal use only
- Needs fixes before beta
- Needs expert review before launch
- Do not launch in current form

Review the app description, prior review findings, issue log, risk classifications, scorecard, and any fixes made.

Explain:
- top 5 risks
- top 5 fixes
- what could go wrong first
- what would be hardest to recover from
- what the builder probably misunderstands
- what evidence is still missing

If the evidence is not enough to decide, say that directly and recommend the safest next step.
```

## Expected Output Format

```text
Recommendation
One of:
- Safe to continue experimenting
- Safe for private/internal use only
- Needs fixes before beta
- Needs expert review before launch
- Do not launch in current form

Reason
- ...

Top 5 Risks
| Risk | Category | Severity | Evidence | Why It Matters |
| --- | --- | --- | --- | --- |

Top 5 Fixes
| Fix | Risk Reduced | Owner | Verification |
| --- | --- | --- | --- |

What Could Go Wrong First
- ...

Hardest Thing To Recover From
- ...

Likely Builder Misunderstanding
- ...

Missing Evidence
- ...

Decision Conditions
- Launch only if...
- Delay if...
- Get expert help if...
```

## Follow-Up Prompts

- Rewrite this as a concise decision memo for a non-technical founder.
- Rewrite this as a developer task list with acceptance criteria.
- Which risks remain after the proposed fixes?
- What should be re-reviewed after fixes are complete?

## Red Flags To Look For

- The recommendation avoids choosing one of the five options.
- The answer does not mention missing evidence.
- The answer treats private/internal use as risk-free.
- The answer ignores what would be hardest to recover from.
- The answer gives launch approval while high or critical issues remain open.

