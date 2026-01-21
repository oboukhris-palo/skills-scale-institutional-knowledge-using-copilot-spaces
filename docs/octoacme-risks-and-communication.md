# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register

Maintain a simple table with:
- ID
- Description
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Owner
- Mitigation plan
- Status

### Risk Register Table Template

Copy and paste this template to create your project's risk register:

| Risk ID | Description | Impact | Likelihood | Priority | Owner | Mitigation Plan | Status | Last Updated |
|---------|-------------|--------|------------|----------|-------|-----------------|--------|--------------|
| R-001 | Brief risk description | High/Med/Low | High/Med/Low | Critical/High/Med/Low | Name | Actions to reduce risk | Open/Mitigated/Closed/Accepted | YYYY-MM-DD |

### Example Risk Entries

| Risk ID | Description | Impact | Likelihood | Priority | Owner | Mitigation Plan | Status | Last Updated |
|---------|-------------|--------|------------|----------|-------|-----------------|--------|--------------|
| R-001 | Third-party API dependency may have downtime | High | Medium | High | Bob Smith | Implement retry logic, cache responses, have fallback plan | Mitigated | 2024-01-20 |
| R-002 | Key developer on leave during release week | Medium | High | High | Alice Chen | Cross-train two team members, document critical procedures | Mitigated | 2024-01-18 |
| R-003 | Database migration may take longer than scheduled maintenance window | High | Low | Medium | Carol Lee | Test migration on staging with production data volume, prepare rollback script | Open | 2024-01-21 |

**Note**: Link significant risk mitigation decisions to the [Decision Log](./octoacme-decision-log.md) for traceability.

## Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduced via actions, contingency plans
- Monitor: review at weekly syncs and update status
- Document: record key risk decisions in [Decision Log](./octoacme-decision-log.md)

## Stakeholder Communication
- Identify stakeholder groups and communication needs (e.g., engineering, sales, support)
- Provide regular updates (weekly or milestone-based)
- Use a single source of truth (project README or release doc) for status

### Stakeholder Update Checklist
- [ ] Identify all stakeholder groups (engineering, product, sales, support, executives)
- [ ] Determine communication frequency and preferred channels for each group
- [ ] Prepare update using the Weekly Status Template (see Communication Templates section)
- [ ] Highlight key decisions from [Decision Log](./octoacme-decision-log.md) that affect stakeholders
- [ ] Include risks from Risk Register that require visibility or escalation
- [ ] Share via agreed channels (email, Slack, wiki page)
- [ ] Solicit feedback and answer questions
- [ ] Document any new decisions or action items
- [ ] Schedule next update

## Communication Templates

### Weekly Status Template:
- Progress this week:
- Next steps:
- Risks & blockers:
- Ask / decisions needed:

### Incident Communication

#### Incident Escalation Checklist
- [ ] Assess incident severity (P0/Critical, P1/High, P2/Medium, P3/Low)
- [ ] Notify on-call engineer and incident commander
- [ ] Create incident channel/room for coordination
- [ ] Notify affected stakeholders (customers, support, sales) based on severity
- [ ] Provide initial status update within 15 minutes for P0, 30 minutes for P1
- [ ] Assign roles: Incident Commander, Communications Lead, Technical Lead
- [ ] Document timeline and actions taken in real-time
- [ ] Provide regular updates every 30-60 minutes until resolved
- [ ] Follow [Hotfix Process](./octoacme-release-and-deployment.md#hotfix-process) if code changes are needed
- [ ] Announce resolution and impact summary
- [ ] Document incident decisions in [Decision Log](./octoacme-decision-log.md)
- [ ] Schedule post-incident retrospective within 48 hours

#### Incident Communication Template
- **Incident ID**: INC-XXX
- **Severity**: P0/P1/P2/P3
- **Status**: Investigating / Identified / Monitoring / Resolved
- **Impact**: Who/what is affected
- **Triage summary**: What we know so far
- **Actions being taken**: Current response efforts
- **Expected timeline**: ETA for resolution (or next update if unknown)
- **Updates**: Link to status page or update channel
- **Post-incident review**: Blameless retrospective scheduled [date/time]

## Escalation Paths
- Team-level -> PM -> Product Lead -> Sponsor
- For security incidents, follow the security incident runbook and notify Security on-call
