# 06 -- Operational Readiness

## Purpose

Use this prompt to review whether the system can be run, monitored, supported, backed up, restored, and fixed when something goes wrong.

## When To Use This Prompt

Use this before internal rollout, beta, production launch, customer demos, or handoff to another person.

## Copy/Paste Prompt

```text
You are reviewing operational readiness for an AI-assisted build.

Assume the app is running at 3AM and the original builder is unavailable. Assume users are affected, logs are noisy, a dependency is down, and someone needs to decide whether to rollback.

Do not assume that "deployed" means "operable".

Review:
- deployment process
- environment configuration
- secrets handling
- logs
- metrics
- alerts
- error tracking
- backup and recovery
- restore testing
- rollback plan
- support process
- incident response
- admin tools
- dependency outages
- data migration risks
- production access controls
- runbooks and documentation

For each gap, explain the operational consequence, how it would be detected, and what minimum readiness step is needed.
```

## Expected Output Format

```text
Operational Readiness Summary
- ...

Operational Gaps
| Gap | Category | Severity | Evidence | Consequence | Minimum Readiness Step |
| --- | --- | --- | --- | --- | --- |

Launch Blockers
- ...

Runbook Items Needed
- ...
```

## Follow-Up Prompts

- What should be monitored on day one?
- What should trigger an alert?
- What should be in the rollback plan?
- What does a support person need to know to handle common failures?

## Red Flags To Look For

- No one knows where logs are.
- There is no tested restore path.
- Secrets are changed manually with no record.
- Deployments cannot be rolled back.
- Only the original builder understands how to operate the system.

