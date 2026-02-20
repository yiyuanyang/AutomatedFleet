# Protocol — Logging

## Purpose

Defines what must be logged, how, and where. All operational and decision processes must be logged without omission (Constitution Article III, Section 6).

## What Must Be Logged

### Decisions

- Every decision made by any agent, with reasoning.
- Group of Deciders votes and outcomes, including dissenting opinions.
- Product Owner directives and steering responses.
- Escalation outcomes.

### Deliberations

- All product design discussions (these form the Project Rationale).
- Architecture and planning discussions.
- Execution plan revisions and why they were made.

### Debates

- All substantive disagreements between agents.
- Arguments from each side.
- Resolution and which party's position was accepted.
- Genuine debates (where real disagreement occurred) are additionally flagged as precedent-eligible.

### Reviews

- All pre-implementation plan reviews and their outcomes.
- All post-implementation code reviews — feedback, responses, iterations.
- Approval and rejection decisions with reasoning.

### Audit

- All audit findings, root cause analyses, and proposed fixes.

### Process Events

- Agent spin-up and spin-down events.
- Task assignments and completions.
- Emergency change injections and responses.
- Status transitions in the execution plan.

## Log Format

Each log entry must include:

| Field | Description |
| ----- | ----------- |
| Timestamp | When the event occurred |
| Agent | Which agent produced the entry |
| Role | The agent's role (e.g., Implementer, Reviewer, Auditor) |
| Event type | Category (decision, debate, review, audit, process) |
| Content | The substantive content of the entry |
| References | Links to related entries, rules, or artifacts |

## Storage

Logs are stored in a project-specific location defined in the execution plan. The storage mechanism must support:

- Append-only writes (logs are never modified or deleted).
- Queryable by agent, role, event type, and time range.
- Accessible to the Auditor at all times.

## Precedent Flagging

When a debate results in a substantive ruling or sets a new interpretation:

1. Flag the log entry as precedent-eligible.
2. The Auditor reviews precedent-eligible entries and determines whether to codify them.
3. Codified precedents may be elevated to subordinate rules per Constitution Article V.

## Scripts

Scripts for automated logging (capturing agent output, PR review threads, status changes) will be defined in `rules/scripts/`. These scripts should minimize the manual logging burden on agents.
