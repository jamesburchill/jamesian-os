# Launch Readiness Checklist

Use this before letting real users depend on the system. For anything sensitive, public, paid, regulated, or business-critical, use this checklist before expert review, not instead of it.

## Product And Scope

- [ ] The purpose is clear.
- [ ] The intended users are clear.
- [ ] The launch audience is limited and defined.
- [ ] Known limitations are documented.
- [ ] Out-of-scope use is documented.

## Security And Privacy

- [ ] Authentication has been reviewed.
- [ ] Authorization has been reviewed server-side.
- [ ] Admin access is limited.
- [ ] Secrets are not in source code, client code, logs, or shared screenshots.
- [ ] Sensitive data is not logged unnecessarily.
- [ ] Privacy-sensitive data collection is understood.
- [ ] Dependency risks have been reviewed.
- [ ] High and critical security findings are closed or escalated to an expert.

## Data Integrity

- [ ] Required fields are enforced.
- [ ] Server-side validation exists for important inputs.
- [ ] Duplicate submissions and repeated webhooks are handled.
- [ ] Important writes are protected against partial failure.
- [ ] Backups are configured.
- [ ] Restore has been tested or expert help has been scheduled.

## Reliability And Operations

- [ ] Errors are handled without exposing sensitive internals.
- [ ] Logs are accessible to the right people.
- [ ] Important failures are observable.
- [ ] Alerts exist for critical failures.
- [ ] There is a support contact or owner.
- [ ] There is a rollback plan.
- [ ] Deployment steps are documented.
- [ ] Environment variables are documented with secret values removed.

## Cost And Abuse

- [ ] Paid services are identified.
- [ ] Usage limits are set where possible.
- [ ] Billing alerts are set.
- [ ] Public endpoints have appropriate rate limits.
- [ ] Uploads, AI calls, jobs, and emails have practical limits.
- [ ] Abuse scenarios have been reviewed.

## Maintainability

- [ ] Setup instructions exist.
- [ ] The data model is explained.
- [ ] Risky workflows are documented.
- [ ] Known issues are tracked.
- [ ] Tests or manual verification steps cover the riskiest paths.
- [ ] Another person can understand how to run and support the system.

## Launch Decision

- [ ] No critical issues remain open.
- [ ] No high launch-blocking issues remain open.
- [ ] Remaining medium and low issues are logged.
- [ ] Missing evidence is documented.
- [ ] The launch decision is one of: launch, limited launch, delay, or get expert help.
- [ ] A rollback or shutoff path exists.

