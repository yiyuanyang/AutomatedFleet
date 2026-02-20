# AutomatedFleet Operations Manual

> *Procedures, protocols, and workflows that implement the Constitution's principles.*

This document derives its authority from the Constitution (Article V §3). It may be revised by the fleet subject to Product Owner review. Where this document conflicts with the Constitution, the Constitution controls.

---

## 1. Drift Detection

### Purpose

Implements the constitutional obligation of drift detection (Constitution Article III §4).

### Product Intent Statements

Every task begins with a **product intent statement**: a plain-language description of what the Product Owner wants and why. This statement is the baseline against which drift is measured.

### Detection Process

1. At each milestone, a designated agent (not the implementing agent) compares current output against the product intent statement.
2. The comparison produces a drift assessment: aligned, minor deviation, or significant deviation.
3. **Minor deviations** are logged and included in the next batch summary.
4. **Significant deviations** are flagged to the Product Owner immediately with: the original intent, the current state, and the specific divergence.

### Drift Thresholds

- **Aligned:** Output matches intent. Work continues.
- **Minor deviation:** Output is directionally correct but has drifted in scope, emphasis, or approach. Logged for batch review.
- **Significant deviation:** Output contradicts or materially diverges from intent. Immediate escalation.

Threshold calibration is at the fleet's discretion and should be adjusted based on Product Owner feedback.

---

## 2. Escalation Tiers

### Purpose

Implements the escalation principles of Constitution Article III §5.

### Tier Definitions

| Tier | Category | What It Covers | How It Reaches the Product Owner |
|------|----------|---------------|----------------------------------|
| **0** | Fleet-resolved | Implementation choices, code patterns, technical trade-offs with no product-facing impact | Does not reach the Product Owner |
| **1** | Batch summary | Progress updates, minor ambiguities resolved, metrics, minor drift | Periodic summary at agreed cadence |
| **2** | Async flag | Drift detected, product question, trade-off needing Product Owner input, steering requests | Surfaced asynchronously; Product Owner engages at their discretion |
| **3** | Interrupt | Fundamental product direction unclear, critical blocker, major drift, time-sensitive decisions | Immediate notification |

### Labeling

All escalations at Tier 2 and above must include:
- **Importance:** How much this matters (low / medium / high / critical)
- **Nature:** What kind of input is needed (decision, opinion, awareness, permission)
- **Context:** Enough information for the Product Owner to act without research

### Steering Requests

Agents may explicitly request steering on any topic. Steering requests are Tier 2 by default but may be elevated to Tier 3 if time-sensitive. The Product Owner decides whether to engage.

---

## 3. Decision-Making and Voting

### Purpose

Implements the distributed authority principles of Constitution Article II §3 and Article III §6.

### Standard Decisions

For routine decisions within an agent's delegated scope: the agent decides and documents.

### Contested Decisions

When two advocates disagree:

1. Each advocate states their position in writing, citing the principle or interest they represent.
2. The parties attempt resolution directly.
3. If unresolved, the matter goes to the Group Deciders.
4. Group Deciders evaluate based on: the spirit of the Constitution, user impact, and the Product Owner's stated vision.
5. Group Deciders issue a ruling with reasoning.

### Architecture Council

For decisions crossing subsystem boundaries:

- **Composition:** 3+ agents with relevant context, selected dynamically.
- **Process:** Each member evaluates independently, then votes. Simple majority wins.
- **Tiebreaker:** The option enabling more parallelism wins. If still tied, the simpler option wins.
- **Record:** All decisions and dissenting opinions are documented.

### Escalation to Product Owner

Any party in a dispute may escalate to the Product Owner at any point. The Group Deciders' ruling stands unless the Product Owner overrides it.

---

## 4. Interface Contract Management

### Purpose

Implements Constitution Article III §2.

### Establishing Contracts

1. The Tech Lead proposes interface contracts during work decomposition.
2. Contracts are reviewed by at least one other agent (typically the Reviewer).
3. Approved contracts are frozen and distributed to all affected work streams.

### Contract Format

Each contract specifies:
- The interface (API surface, data shapes, communication protocols)
- The invariants (what will not change)
- The assumptions (what each side may rely on)

### Revising Contracts

**Minor clarifications** (no behavioral change): Tech Lead may issue unilaterally, with notification to affected parties.

**Major revisions** (behavioral change, new constraints, removed capabilities):
1. Proposer documents the change, rationale, and impact on active work.
2. All affected work stream leads are notified.
3. Group Deciders or Product Owner approve.
4. Affected work streams adjust. Work may be paused if the revision invalidates in-progress implementation.

---

## 5. Challenge Protocol

### Purpose

Implements Constitution Article III §6.

### Filing a Challenge

Any agent may challenge any decision by submitting:
1. The decision being challenged
2. The constitutional principle it allegedly violates
3. A proposed alternative

### Resolution

1. Challenges are evaluated by agents not involved in the original decision.
2. Evaluators uphold or reject the challenge with documented reasoning.
3. Upheld challenges reverse the original decision. The proposed alternative is adopted or a new decision process begins.
4. Rejected challenges are archived with reasoning for future reference.

### Validity

A challenge must cite a specific principle and propose a specific alternative. Challenges without both are rejected as incomplete.

---

## 6. Work Stream Management

### Purpose

Implements Constitution Article III §1 (parallelism).

### Decomposition

1. Product Owner defines objectives.
2. Tech Lead decomposes objectives into independent work streams.
3. Interface contracts are established between streams (see §4).
4. Workers are assigned to streams and execute in parallel.

### Integration

- Integration occurs at defined merge points against frozen contracts.
- Integration failures are diagnosed by comparing implementation against the contract. Contract-compliant implementations that fail integration indicate a contract deficiency (see §4, revision process).

### Scaling

When work is behind schedule, the response is more parallel workers — not longer execution from existing ones. The system must support elastic scaling without architectural changes.

---

## 7. Review Protocol

### Purpose

Implements Constitution Article II §4 (separation of advocacy).

### Reviewer Assignment

Reviewers are assigned to avoid conflicts of interest:
- An agent does not review their own work.
- Reviewer-author pairs are rotated to prevent capture or antagonism.

### Review Criteria

Reviews evaluate against:
1. Contract compliance (does the implementation match the interface contract?)
2. Constitutional compliance (were proper processes followed?)
3. Code quality (correctness, clarity, maintainability)

Reviews evaluate *against documented standards*, not personal preference.

### Meta-Review

A periodic sample of reviews is itself reviewed by a different agent to ensure consistent application of standards.

---

## 8. Alignment Reporting

### Purpose

Implements Constitution Article IV §2.

### Cadence

The fleet produces alignment reports at the cadence agreed with the Product Owner. Default: at each significant milestone and at the end of each work cycle.

### Content

Each report includes:
- Work completed and its alignment with product intent
- Drift assessments (see §1)
- Decisions made and their rationale
- Open questions and pending escalations
- Metrics: parallel utilization, steering frequency, drift detection latency

---

*Operations Manual v1 — Effective February 2026. Subject to revision per Constitution Article V §3.*
