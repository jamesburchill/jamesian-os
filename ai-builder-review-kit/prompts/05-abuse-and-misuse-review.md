# 05 -- Abuse And Misuse Review

## Purpose

Use this prompt to examine how the system could be misused, abused, spammed, scraped, overloaded, manipulated, or used against other people.

## When To Use This Prompt

Use this for public forms, signups, uploads, messaging, AI features, search, comments, sharing, invitations, payments, automation, or integrations.

## Copy/Paste Prompt

```text
You are reviewing abuse and misuse risks for an AI-assisted build.

Assume the system is used by someone impatient, confused, or hostile. Assume someone wants free resources, private data, spam delivery, account takeover, reputation damage, or service disruption.

Do not only review accidental misuse. Think like an abuser, then recommend practical controls.

Review:
- signup and login abuse
- password reset abuse
- invitation abuse
- spam and messaging abuse
- file upload abuse
- scraping and enumeration
- rate limit gaps
- AI prompt injection or output abuse where relevant
- payment or trial abuse
- resource exhaustion
- impersonation
- privacy harm
- legal or compliance exposure
- support burden

For each abuse case, explain who is harmed, how likely it is, what signals would reveal it, and what minimum controls are needed.
```

## Expected Output Format

```text
Abuse Scenarios
| Scenario | Harmed Party | Category | Severity | Abuse Path | Signals | Controls |
| --- | --- | --- | --- | --- | --- | --- |

Highest Priority Controls
- ...

Accepted Risks
- ...
```

## Follow-Up Prompts

- What rate limits should exist and where?
- How could someone use this system to harm another user?
- What abuse signals should be logged or alerted?
- What controls are appropriate for beta without overbuilding?

## Red Flags To Look For

- Public endpoints have no rate limits.
- User enumeration is easy.
- Uploaded files are trusted.
- AI features can be used to process secrets, private data, or harmful instructions without controls.
- Abuse would only be noticed after a complaint.

