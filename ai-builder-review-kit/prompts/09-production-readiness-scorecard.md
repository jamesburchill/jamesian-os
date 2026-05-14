# 09 -- Production-Readiness Scorecard

## Purpose

Use this prompt to produce a plain-language 100-point production-readiness scorecard. The score is not proof of safety. It is a structured way to identify weak areas and decide what needs more review.

## When To Use This Prompt

Use this after the earlier review prompts, once you have enough evidence to score the system.

## Copy/Paste Prompt

```text
You are scoring production readiness for an AI-assisted build.

Do not inflate the score to be encouraging. If evidence is missing, score conservatively and mark the category as unverified.

Use a 100-point scorecard with these categories. Each category is worth the listed points:

- Purpose clarity: 5
- Data model clarity: 7
- Input validation: 8
- Authentication: 8
- Authorization: 8
- Secrets handling: 7
- Error handling: 7
- Logging/observability: 7
- Backup/recovery: 7
- Dependency management: 6
- Cost controls: 6
- Abuse resistance: 7
- Maintainability: 7
- Documentation: 5
- Launch rollback plan: 5

For each category:
- give a score
- explain the evidence
- name what is missing
- identify the highest-risk gap
- recommend the next fix

If a category does not apply, explain why and redistribute no points. Do not hide the non-applicable category. If you are unsure whether it applies, score it conservatively.
```

## Expected Output Format

```text
Total Score: __ / 100

Scorecard
| Category | Max Points | Score | Evidence | Missing Evidence | Highest-Risk Gap | Next Fix |
| --- | ---: | ---: | --- | --- | --- | --- |

Score Interpretation
- 85-100: Stronger candidate, still verify high-risk areas.
- 70-84: Promising, but likely needs targeted fixes before broader use.
- 50-69: Not ready for production without meaningful remediation.
- Below 50: Treat as experimental until reviewed and repaired.

Launch-Relevant Blockers
- ...
```

## Plain-Language Scoring Guidance

### Purpose clarity -- 5 points

Full points require a clear explanation of what the system does, who it serves, what problem it solves, and what it intentionally does not do. Low scores mean the system is hard to evaluate because its purpose is vague.

### Data model clarity -- 7 points

Full points require clear entities, relationships, ownership rules, lifecycle states, and retention expectations. Low scores mean the system may store or change data without clear meaning.

### Input validation -- 8 points

Full points require server-side validation for required fields, types, formats, sizes, states, and malicious input. Low scores mean bad data can enter and spread.

### Authentication -- 8 points

Full points require clear login, session, password reset, identity provider, and account recovery behaviour. Low scores mean the system may not reliably know who is using it.

### Authorization -- 8 points

Full points require server-side checks that each user can only access and change what they are allowed to. Low scores mean users may cross account, role, tenant, project, or admin boundaries.

### Secrets handling -- 7 points

Full points require secrets to be stored outside source code, excluded from client bundles, rotated when needed, and protected in logs and deployment settings. Low scores mean credentials may leak or be hard to rotate.

### Error handling -- 7 points

Full points require predictable handling of failed inputs, failed dependencies, failed jobs, and user-visible errors. Low scores mean failures may corrupt data, confuse users, or disappear.

### Logging/observability -- 7 points

Full points require enough logs, metrics, traces, or error reports to diagnose serious issues without exposing sensitive data. Low scores mean operators may not know what failed or why.

### Backup/recovery -- 7 points

Full points require defined backups, restore steps, retention, and at least one tested recovery path. Low scores mean data loss may be permanent or recovery may be improvised.

### Dependency management -- 6 points

Full points require known dependencies, version control, update process, vulnerability awareness, and fallback plans for important services. Low scores mean hidden dependency risk can break the system.

### Cost controls -- 6 points

Full points require limits, quotas, alerts, and usage tracking for paid services, AI calls, storage, email, jobs, and traffic. Low scores mean cost can grow without warning.

### Abuse resistance -- 7 points

Full points require practical controls against spam, scraping, enumeration, resource exhaustion, impersonation, and misuse. Low scores mean the app may become a tool for harm or disruption.

### Maintainability -- 7 points

Full points require understandable structure, consistent patterns, low duplication, reviewed generated code, and clear change points. Low scores mean future fixes may be slow and risky.

### Documentation -- 5 points

Full points require setup, configuration, deployment, support, and known-risk documentation. Low scores mean handoff and incident response depend on memory.

### Launch rollback plan -- 5 points

Full points require a clear way to rollback code, config, data migrations, feature flags, or public access. Low scores mean a bad launch may be difficult to reverse.

## Follow-Up Prompts

- Which five categories most reduce launch confidence?
- What evidence would most improve the score?
- What is the minimum fix set to move this from experimental to private beta?
- Which category is most likely overrated and why?

## Red Flags To Look For

- The score is high despite missing evidence.
- Security and authorization are scored from UI behaviour only.
- Backup points are awarded without a restore test.
- Cost controls are ignored because current usage is low.
- The score is treated as a launch approval.

