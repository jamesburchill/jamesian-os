# 02 -- Security And Trust Boundaries

## Purpose

Use this prompt to review who or what the system trusts, where sensitive data moves, and where attackers or confused users could cross boundaries.

## When To Use This Prompt

Use this when the system has user accounts, admin screens, APIs, forms, uploads, integrations, webhooks, payment flows, private data, tokens, or external services.

## Copy/Paste Prompt

```text
You are reviewing security and trust boundaries for an AI-assisted build.

Assume this application is already compromised. Assume at least one user is impatient, confused, or hostile. Assume secrets, tokens, IDs, URLs, files, and API responses may be exposed in unexpected places.

Do not give shallow reassurance. If you cannot verify a security claim from the evidence I provide, mark it as "unverified".

Map the trust boundaries:
- browser or client
- server or backend
- database
- file storage
- third-party APIs
- authentication provider
- admin tools
- background jobs
- webhook senders
- payment or billing provider
- logs and analytics

Review:
- authentication concerns
- authorization concerns
- privilege escalation paths
- insecure direct object reference risks
- secrets handling
- dependency risks
- webhook verification
- file upload risks
- admin access risks
- logging of sensitive data
- privacy risks
- session handling
- rate limiting and abuse controls

For each issue, classify risk category and severity. Explain the evidence, likely impact, and minimum acceptable fix.
```

## Expected Output Format

```text
Trust Boundary Map
| Boundary | Trusted Inputs | Untrusted Inputs | Sensitive Data | Main Risk |
| --- | --- | --- | --- | --- |

Security Findings
| Finding | Category | Severity | Evidence | Attack Scenario | Minimum Fix |
| --- | --- | --- | --- | --- | --- |

Unverified Claims
- ...

Manual Checks Needed
- ...
```

## Follow-Up Prompts

- Show me the most likely privilege escalation path.
- What would an attacker try first?
- Which secrets could leak through logs, URLs, errors, client code, or screenshots?
- What authorization checks should exist on each route, action, or data object?

## Red Flags To Look For

- The app trusts client-side checks.
- Admin-only actions do not have server-side authorization.
- User IDs, file IDs, project IDs, or account IDs can be changed by the user.
- Secrets appear in client code, logs, `.env` files committed to source control, or shared screenshots.
- Webhooks are accepted without signature verification.

