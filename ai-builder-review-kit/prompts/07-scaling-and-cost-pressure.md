# 07 -- Scaling And Cost Pressure

## Purpose

Use this prompt to find places where usage growth, background work, AI calls, storage, APIs, traffic, or mistakes could make the system slow, expensive, or unavailable.

## When To Use This Prompt

Use this when the system may get public traffic, process files, call AI models, send email, run scheduled jobs, sync data, use paid APIs, store media, or support multiple users.

## Copy/Paste Prompt

```text
You are reviewing scaling and cost pressure for an AI-assisted build.

Assume traffic spikes unexpectedly. Assume a user uploads a large file, repeats an action many times, or triggers expensive work. Assume third-party APIs charge per request, token, job, email, storage unit, or minute.

Do not give generic scaling advice. Identify likely pressure points from the evidence I provide.

Review:
- expensive database queries
- missing pagination
- background job growth
- AI token or model cost runaway
- storage growth
- file processing limits
- email or notification volume
- third-party API quotas
- retry storms
- concurrency issues
- cache assumptions
- rate limits
- billing alerts
- cost controls
- degraded-mode behaviour

For each issue, explain what growth or misuse triggers it, the likely cost or reliability impact, and the simplest practical control.
```

## Expected Output Format

```text
Pressure Points
| Pressure Point | Trigger | Category | Severity | Cost Impact | Reliability Impact | Control |
| --- | --- | --- | --- | --- | --- | --- |

Missing Limits
- ...

Cost Controls Needed
- ...

Performance Checks Needed
- ...
```

## Follow-Up Prompts

- Where should I add hard limits before launch?
- What usage metric would warn me before costs run away?
- Which features should degrade gracefully when a dependency is slow or expensive?
- What should I test with 10x current usage?

## Red Flags To Look For

- No pagination on growing lists.
- No limits on AI calls, uploads, retries, or background jobs.
- No budget alerts for paid APIs.
- One user can trigger work that affects all users.
- Cost is only checked after billing arrives.

