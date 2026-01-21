# OctoAcme — Decision Log

## Purpose
Provide a reusable template for capturing major project decisions, their rationale, alternatives considered, and outcomes. This ensures transparency, facilitates knowledge sharing, and enables teams to understand the "why" behind key choices.

## When to Use
Document decisions that:
- Impact project scope, architecture, or technical direction
- Affect multiple teams or stakeholders
- Have significant cost, timeline, or risk implications
- Require future reference or may need to be revisited

## Decision Log Template

Copy the table below and add entries as major decisions are made:

| Decision ID | Date | Decision Summary | Context & Problem | Alternatives Considered | Decision Made | Rationale | Owner | Status | Outcome / Notes |
|-------------|------|------------------|-------------------|------------------------|---------------|-----------|-------|--------|-----------------|
| DEC-001 | YYYY-MM-DD | Brief title of decision | What problem are we solving? | What other options did we evaluate? | What did we decide? | Why did we choose this? | Name | Proposed / Approved / Implemented / Revisited | Results, lessons learned, or follow-up actions |

## Example Entry

| Decision ID | Date | Decision Summary | Context & Problem | Alternatives Considered | Decision Made | Rationale | Owner | Status | Outcome / Notes |
|-------------|------|------------------|-------------------|------------------------|---------------|-----------|-------|--------|-----------------|
| DEC-001 | 2024-01-15 | Choose PostgreSQL for primary database | Need scalable, ACID-compliant database for user data | MongoDB (document store), MySQL (relational) | Use PostgreSQL 15+ | Strong ACID compliance, mature ecosystem, team expertise | Alice Chen | Implemented | Migration completed successfully; performance meets requirements |

## Instructions

1. **Assign a unique Decision ID** - Use sequential numbering (DEC-001, DEC-002, etc.)
2. **Date** - When the decision was made (YYYY-MM-DD format)
3. **Decision Summary** - One-line description
4. **Context & Problem** - What challenge or question prompted this decision?
5. **Alternatives Considered** - What other options were evaluated? (shows due diligence)
6. **Decision Made** - The chosen approach
7. **Rationale** - Why this option was selected over others
8. **Owner** - Person accountable for the decision
9. **Status** - Current state (Proposed, Approved, Implemented, Revisited)
10. **Outcome / Notes** - Results after implementation, lessons learned, or follow-up needed

## Best Practices

- **Link from checklists**: Reference this Decision Log in project planning, release, and risk management checklists
- **Keep it updated**: Review and update status as decisions are implemented
- **Be concise**: Aim for clarity, not exhaustive detail
- **Archive old decisions**: Move implemented decisions to a separate archive section if the log grows large
- **Review during retrospectives**: Use decision outcomes to inform future choices

## Integration with Other Docs

- Reference key decisions in the [Risk Register](./octoacme-risks-and-communication.md) if they mitigate specific risks
- Link decisions to [Release Notes](./octoacme-release-and-deployment.md) for traceability
- Include decision review as part of [Retrospectives](./octoacme-retrospective-and-continuous-improvement.md)
