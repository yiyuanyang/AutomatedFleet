# Protocol — Implementation

## Purpose

Defines the workflow from task assignment through implementation to submission for review.

## Preconditions

- The execution plan is finalized (see `architecture-planning.md`).
- The Tech Lead has assigned a fragment to this Implementer.
- The Reviewer is active.

## Process

### Step 1: Receive Assignment

The Tech Lead spins up the Implementer with:
- The Implementer role document (`rules/roles/implementer.md`).
- The assigned execution plan fragment.
- Relevant interface contracts.
- Any additional context specified in the role document.

### Step 2: Propose Fragment Implementation Plan

Before writing any code, the Implementer proposes an implementation plan to the Reviewer:

1. **What will be built**: Summary of the fragment's purpose.
2. **Approach**: Design decisions, patterns to use, key algorithms.
3. **Files**: Which files will be created or modified.
4. **Interfaces**: How this fragment connects to others (referencing interface contracts).
5. **Tests**: What test cases will be written.

### Step 3: Reviewer Confirmation

1. The Reviewer evaluates the proposed plan against the execution plan.
2. Back and forth until confirmed. The Reviewer may request changes to the approach, additional test cases, or clarification.
3. The Implementer does not begin coding until the Reviewer confirms.

### Step 4: Implement

1. Follow the confirmed plan and the execution plan spec as closely as possible.
2. Write all code in a feature branch (see branching strategy in the execution plan).
3. Write tests alongside implementation.
4. Ensure all tests pass locally.

### Step 5: Submit for Review

1. Create a pull request with:
   - Clear description of what was implemented.
   - Reference to the execution plan fragment.
   - Test results.
2. The Reviewer reviews per `review.md`.

### Step 6: Address Feedback

1. Respond to all review comments.
2. If feedback is correct, incorporate changes.
3. If disagreeing, provide specific reasoning.
4. Iterate until the Reviewer approves.
5. If a dispute cannot be resolved, escalate per `escalation.md`.

### Step 7: Merge

Once the Reviewer approves, the work is merged per the branching strategy defined in the execution plan.

## Logging

All implementation discussions, plan proposals, and review interactions must be logged per `logging.md`.
