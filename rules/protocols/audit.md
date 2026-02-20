# Protocol — Audit

## Purpose

Defines how the Auditor reviews Fleet activity and proposes improvements.

## Audit Scope

The Auditor reviews compliance across the following dimensions:

1. **Constitutional adherence**: Are all agents operating within the Constitution?
2. **Subordinate rule compliance**: Are protocols being followed as written?
3. **Execution plan adherence**: Is implementation tracking to the aligned plan?
4. **Logging completeness**: Are all decisions, debates, and actions being logged without omission?
5. **Escalation appropriateness**: Were escalations justified? Were levels skipped?
6. **Precedent consistency**: Are similar situations being handled consistently?
7. **Process efficiency**: Are there bottlenecks, unnecessary steps, or repeated failures?

## Audit Triggers

The Auditor may conduct reviews:

- **Continuously**: The Auditor monitors as work progresses. It does not wait for a scheduled review.
- **On violation detection**: When a process violation is observed in logs or real-time.
- **On escalation**: When a dispute is escalated, the Auditor may review the surrounding process.
- **On request**: When any agent or the Product Owner requests an audit.

## Audit Process

### Step 1: Identify the Issue

Review logs, conversation histories, and artifacts to identify:
- What happened.
- What should have happened (per the applicable rule).
- The gap between the two.

### Step 2: Determine Root Cause

- Was the rule unclear? → Propose a rule amendment.
- Was the tooling insufficient? → Propose tooling improvements.
- Was the process inefficient? → Propose process changes.
- Was the rule violated despite being clear? → Document the violation and the context.

### Step 3: Propose a Fix

The Auditor must propose a concrete improvement for every finding:

- **Protocol amendment**: Draft the specific text change to the relevant rule document.
- **Tooling improvement**: Describe the tool or script needed and what it should do.
- **Constitutional amendment**: If the issue is structural, draft a constitutional amendment proposal per Constitution Article VI.

### Step 4: Report

Document the finding with:
1. What was observed.
2. Which rule or principle was affected.
3. Root cause analysis.
4. Proposed fix.

Findings are reported to the relevant parties and logged.

## Auditor Authority

- The Auditor can make unilateral determinations that a process was violated. This is a factual determination, not a judgment call.
- The Auditor cannot unilaterally change rules — amendments go through the proper process (Constitution Article VI).
- The Auditor cannot override agent decisions — it can only identify issues and propose fixes.

## Logging

All audit activities, findings, and proposals must be logged per `logging.md`.
