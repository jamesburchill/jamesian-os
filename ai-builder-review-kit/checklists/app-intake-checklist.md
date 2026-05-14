# App Intake Checklist

Use this checklist before running the prompt pack. The review will be weaker if the reviewer has to guess.

## Basic Description

- [ ] What is the app, website, automation, SaaS prototype, script, or tool called?
- [ ] What problem does it solve?
- [ ] Who uses it?
- [ ] Who administers it?
- [ ] Is it experimental, internal, beta, or production-facing?
- [ ] What would count as a serious failure?

## Users And Access

- [ ] Does it have user accounts?
- [ ] Does it have roles, teams, tenants, projects, or permissions?
- [ ] Are there admin users?
- [ ] How are users invited, created, removed, or disabled?
- [ ] How does password reset or account recovery work?
- [ ] What should one user never be able to see or change?

## Data

- [ ] What data does the system collect?
- [ ] What data does it create or modify?
- [ ] Does it handle personal, sensitive, financial, legal, health, or confidential data?
- [ ] Where is data stored?
- [ ] How long is data kept?
- [ ] How is data deleted?
- [ ] How is data backed up?
- [ ] Has restore been tested?

## Inputs And Integrations

- [ ] What forms, uploads, APIs, webhooks, imports, or automations accept input?
- [ ] Which inputs come from users?
- [ ] Which inputs come from third parties?
- [ ] Which inputs come from AI-generated output?
- [ ] What happens when input is missing, malformed, duplicated, too large, or malicious?

## Deployment And Operations

- [ ] Where does it run?
- [ ] How is it deployed?
- [ ] What environment variables or secrets does it need?
- [ ] Where are logs?
- [ ] Where are errors reported?
- [ ] Who gets alerts?
- [ ] How is rollback handled?
- [ ] Who supports it if it breaks?

## Cost And Limits

- [ ] Which paid services does it use?
- [ ] Does it use AI models, paid APIs, storage, email, SMS, jobs, or serverless functions?
- [ ] Are usage limits set?
- [ ] Are billing alerts set?
- [ ] Can one user trigger expensive work?

## Evidence To Provide To The Reviewing AI

- [ ] Plain-language description
- [ ] Screenshots or screen recording
- [ ] User roles and permissions
- [ ] Data schema or table list
- [ ] API routes or workflow diagram
- [ ] Deployment notes
- [ ] Environment variable list with secret values removed
- [ ] Dependency list
- [ ] Known bugs
- [ ] Logs or error examples
- [ ] Backup and restore notes
- [ ] Current issue list

