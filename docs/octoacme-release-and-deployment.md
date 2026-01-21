# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared
- Key decisions documented in [Decision Log](./octoacme-decision-log.md)

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support
- [ ] Document any deployment decisions in [Decision Log](./octoacme-decision-log.md)

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Hotfix Process

When a critical production issue requires an immediate fix outside the normal release cycle:

### Hotfix Checklist
- [ ] Confirm issue severity and impact (customer-facing, data integrity, security, etc.)
- [ ] Create hotfix branch from production/main branch
- [ ] Implement minimal fix with focused scope
- [ ] Fast-track code review with at least one senior engineer
- [ ] Run targeted tests (unit + integration for affected area)
- [ ] Deploy to staging and verify fix resolves the issue
- [ ] Prepare rollback plan (document revert steps or previous version)
- [ ] Follow [Incident Escalation Checklist](./octoacme-risks-and-communication.md#incident-escalation-checklist)
- [ ] Deploy to production with monitoring
- [ ] Verify fix in production and monitor for 30+ minutes
- [ ] Notify stakeholders using [Incident Communication Template](./octoacme-risks-and-communication.md#incident-communication)
- [ ] Schedule post-incident retrospective within 48 hours
- [ ] Document hotfix decision and outcome in [Decision Log](./octoacme-decision-log.md)
- [ ] Backport fix to main development branch if needed

### Rollback Checklist
- [ ] Identify last known-good release version
- [ ] Notify team and stakeholders of impending rollback
- [ ] Execute rollback via deployment pipeline or manual process
- [ ] Verify service health and functionality after rollback
- [ ] Update status page or communication channels
- [ ] Document rollback decision and next steps in [Decision Log](./octoacme-decision-log.md)
- [ ] Investigate root cause and plan proper fix

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
