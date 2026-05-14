# The AI Builder Review Kit

You built something. Now review it properly.

The AI Builder Review Kit is a practical review framework and prompt pack for people who have used AI-assisted building, vibe coding, no-code, low-code, or AI coding tools to create an app, website, automation, SaaS prototype, script, or internal tool.

AI lowers creation friction. It does not eliminate systems complexity.

Working is not the same as safe, stable, secure, recoverable, or maintainable.

The AI Builder Review Kit gives builders borrowed scar tissue.

## What This Kit Is

This kit helps you pressure-test what you built before production reality does it for you. It gives you structured prompts, checklists, and templates for reviewing risk, security, data integrity, failure modes, abuse, operations, cost pressure, maintainability, and launch readiness.

It is designed to make a reviewing AI work harder. The prompts ask for assumptions, trust boundaries, missing evidence, likely failure points, and concrete fixes instead of shallow reassurance.

## Who This Is For

Use this kit if you built or assembled something with AI-assisted tools and need a calm, practical review before wider use.

It is useful for:

- solo builders and founders
- internal tool makers
- no-code and low-code builders
- product managers testing prototypes
- developers reviewing AI-generated work
- teams preparing a beta or internal rollout
- consultants reviewing client-built systems

## Who This Is Not For

This kit is not a replacement for professional security review, legal review, compliance review, privacy review, accessibility review, or production engineering.

It is not enough for high-risk systems, regulated environments, payment systems, health data, legal data, safety-critical workflows, public authentication systems, or anything where failure could cause serious harm.

If the system handles sensitive data, money, identity, safety, production operations, or legal obligations, use this kit as preparation for expert review -- not as a substitute for it.

## Why Review Still Matters

AI-assisted building is legitimate. It can help people create useful software faster, and it can make technical creation more accessible.

That does not remove the need for review. A tool can help you produce code, workflows, schemas, integrations, and configuration, but it may not understand the full context of your users, data, obligations, threat model, recovery needs, or operating environment.

The question is not whether AI helped you build it. The question is whether the result can survive real use.

## Important Warning

AI responses may be incomplete, outdated, or wrong. Treat every review answer as a lead to verify, not as proof.

Check claims against the actual app, code, configuration, data, logs, dependency versions, hosting settings, access controls, payment settings, and user flows. If the reviewing AI cannot cite evidence from what you provided, treat the answer as an assumption.

## Suggested Workflow

1. Describe the app.
2. Run the intake checklist.
3. Run each prompt pack section.
4. Capture issues.
5. Classify risk.
6. Fix high-risk items.
7. Re-run the review.
8. Decide whether to launch, delay, or get expert help.

## How To Use This Kit

Start by writing a plain-language description of what the system does, who uses it, what data it handles, and where it runs. Include screenshots, diagrams, links, code snippets, environment notes, dependency lists, database schema, hosting details, and any known concerns where possible.

Then work through the files in order:

1. [App intake checklist](checklists/app-intake-checklist.md)
2. [Basic safety review](prompts/01-basic-safety-review.md)
3. [Security and trust boundaries](prompts/02-security-and-trust-boundaries.md)
4. [Data integrity and validation](prompts/03-data-integrity-and-validation.md)
5. [Edge cases and failure modes](prompts/04-edge-cases-and-failure-modes.md)
6. [Abuse and misuse review](prompts/05-abuse-and-misuse-review.md)
7. [Operational readiness](prompts/06-operational-readiness.md)
8. [Scaling and cost pressure](prompts/07-scaling-and-cost-pressure.md)
9. [Maintainability and handoff](prompts/08-maintainability-and-handoff.md)
10. [Production-readiness scorecard](prompts/09-production-readiness-scorecard.md)
11. [Final go/no-go review](prompts/10-final-go-no-go-review.md)

Use these supporting templates as you go:

- [Risk classification checklist](checklists/risk-classification-checklist.md)
- [Launch readiness checklist](checklists/launch-readiness-checklist.md)
- [Audit report template](templates/audit-report-template.md)
- [Issue log template](templates/issue-log-template.md)

## Risk Categories

Use these categories when recording issues:

- Cosmetic
- Usability Risk
- Reliability Risk
- Security Risk
- Data Integrity Risk
- Privacy Risk
- Financial Risk
- Legal/Compliance Risk
- Operational Risk
- Catastrophic Failure Risk

Use these severity levels:

- Low
- Medium
- High
- Critical

## Practical Rule

If the review finds a high or critical issue, do not treat the system as launch-ready until the issue is fixed, verified, and re-reviewed.

If the review depends on missing evidence, gather the evidence before deciding.

