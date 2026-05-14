# 08 -- Maintainability And Handoff

## Purpose

Use this prompt to review whether another person can understand, change, debug, deploy, and support the system without relying on the original builder.

## When To Use This Prompt

Use this before handing work to a developer, onboarding a teammate, preparing a client delivery, or deciding whether to keep building on the current foundation.

## Copy/Paste Prompt

```text
You are reviewing maintainability and handoff readiness for an AI-assisted build.

Assume the original builder is unavailable. Assume a new developer or operator must fix a production issue, add a feature, or audit a risky workflow.

Do not judge the builder. Review the system as something that must be understood and maintained.

Review:
- project structure
- naming clarity
- duplicated logic
- dead or unused code
- hidden assumptions
- dependency risks
- setup instructions
- environment variables
- data model clarity
- test coverage
- error handling patterns
- logging patterns
- documentation gaps
- deployment notes
- ownership boundaries
- parts likely generated without review

For each concern, explain why it makes future change riskier and what documentation, test, refactor, or simplification would help most.
```

## Expected Output Format

```text
Handoff Summary
- ...

Maintainability Findings
| Finding | Category | Severity | Evidence | Future Risk | Recommended Fix |
| --- | --- | --- | --- | --- | --- |

Documentation Needed
- ...

Tests Needed
- ...

Questions For The Builder
- ...
```

## Follow-Up Prompts

- What would confuse a new developer first?
- Which files or workflows should be documented before handoff?
- Which generated-looking code needs human review?
- What should be simplified before adding more features?

## Red Flags To Look For

- Setup depends on undocumented local state.
- Environment variables are not listed or explained.
- There are no tests around risky workflows.
- Similar logic appears in several places.
- The system cannot be explained without reading every file.

