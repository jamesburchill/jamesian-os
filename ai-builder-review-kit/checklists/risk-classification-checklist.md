# Risk Classification Checklist

Use this checklist after the prompt pack identifies issues. Classify each issue by category and severity, then decide what must be fixed before launch or wider use.

## Risk Categories

### Cosmetic

Visual, wording, layout, or polish issues that do not materially affect use, safety, data, money, privacy, operations, or trust.

### Usability Risk

Users may misunderstand, misuse, abandon, or make mistakes because the interface or workflow is unclear.

### Reliability Risk

The system may fail, slow down, time out, duplicate work, lose availability, or behave unpredictably.

### Security Risk

An attacker or unauthorized user may access, change, delete, impersonate, escalate privileges, exploit dependencies, or obtain secrets.

### Data Integrity Risk

Data may become wrong, duplicated, stale, missing, inconsistent, corrupted, or impossible to reconcile.

### Privacy Risk

Personal, sensitive, confidential, or user-specific data may be exposed, over-collected, retained too long, logged, shared, or used unexpectedly.

### Financial Risk

The system may cause unexpected cost, incorrect billing, payment errors, fraud, runaway API usage, or avoidable financial loss.

### Legal/Compliance Risk

The system may create contractual, regulatory, consent, retention, accessibility, licensing, recordkeeping, or jurisdictional exposure.

### Operational Risk

The system may be hard to deploy, monitor, support, recover, rollback, hand off, or operate during an incident.

### Catastrophic Failure Risk

The system may cause severe harm, unrecoverable data loss, major security exposure, serious legal exposure, major financial impact, or prolonged business disruption.

## Severity Levels

### Low

The issue is limited, recoverable, and unlikely to affect safety, trust, sensitive data, money, or core operations.

### Medium

The issue can affect real users, produce support burden, cause confusion, damage data quality, or create a meaningful but contained risk.

### High

The issue can expose sensitive data, allow unauthorized action, corrupt important data, cause significant downtime, create major cost, or block safe launch.

### Critical

The issue can cause severe harm, broad compromise, unrecoverable data loss, legal or compliance crisis, major financial damage, or a launch that should be stopped immediately.

## Classification Questions

- [ ] What category best describes the primary harm?
- [ ] Is there a secondary category?
- [ ] Who is harmed?
- [ ] What data, money, access, or workflow is affected?
- [ ] Can the issue be exploited intentionally?
- [ ] Can the issue happen accidentally?
- [ ] How easy is it to trigger?
- [ ] How hard is it to detect?
- [ ] How hard is it to recover?
- [ ] Does the issue become worse as usage grows?
- [ ] Does the issue require expert review?
- [ ] Should this block launch, beta, or internal use?

## Default Decisions

- [ ] Critical issues block launch.
- [ ] High security, privacy, data integrity, financial, legal/compliance, or catastrophic risks block launch.
- [ ] High operational risks block launch if rollback, recovery, or support is unclear.
- [ ] Medium issues may be acceptable for controlled internal use if they are known, tracked, and bounded.
- [ ] Low issues should still be logged, but they usually should not block learning or experimentation.

