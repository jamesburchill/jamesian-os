# 04 -- Edge Cases And Failure Modes

## Purpose

Use this prompt to explore what happens outside the happy path, especially when services fail, users act unexpectedly, or the app is used at inconvenient times.

## When To Use This Prompt

Use this before beta, launch, handoff, or any workflow that affects users, data, money, identity, files, or operations.

## Copy/Paste Prompt

```text
You are reviewing edge cases and failure modes for an AI-assisted build.

Assume the app is running at 3AM and the original builder is unavailable. Assume users are impatient, confused, distracted, or hostile. Assume networks fail, APIs time out, jobs run twice, files are too large, and data is incomplete.

Avoid shallow reassurance. Identify concrete failure modes and recovery paths.

Review:
- empty states
- invalid states
- missing data
- duplicated data
- large inputs
- slow responses
- failed API calls
- failed payment or billing events
- failed file uploads
- failed background jobs
- retries and idempotency
- race conditions
- concurrency issues
- partial outages
- data recovery
- user-facing error messages
- support and escalation paths

For each failure mode, explain what triggers it, what the user sees, what data is at risk, how the system should respond, and how operators would know it happened.
```

## Expected Output Format

```text
Failure Mode Table
| Failure Mode | Trigger | User Impact | Data Risk | Current Evidence | Required Behaviour | Observability |
| --- | --- | --- | --- | --- | --- | --- |

Most Serious Unknowns
- ...

Recovery Gaps
- ...
```

## Follow-Up Prompts

- Which failures need automated alerts?
- Which failures should be retried, and which should not?
- Where does the app need idempotency?
- What would support staff need to diagnose the top three failures?

## Red Flags To Look For

- Errors are only shown as generic messages with no logs.
- Background jobs can fail silently.
- Retries can duplicate side effects.
- There is no clear recovery process after partial failure.
- The app depends on the original builder being available.

