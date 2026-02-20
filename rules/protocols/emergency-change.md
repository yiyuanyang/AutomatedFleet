# Protocol — Emergency Changes

## Purpose

Defines how the Product Owner injects emergency changes during execution and how the Fleet responds.

## What Is an Emergency Change

An emergency change is a directive from the Product Owner that must be prioritized immediately, even if it conflicts with the current execution plan or product design.

## Process

### Step 1: Product Owner Issues the Emergency

The Product Owner communicates the emergency change through the Auditor with:
- What needs to change.
- Why it is urgent.
- Any constraints on the change.

### Step 2: Group of Deciders Discussion

The Group of Deciders may discuss reasoning and alignment with product motivation:
- This is advisory, not a veto. The Product Owner's emergency stands.
- The discussion is logged for the Project Rationale.
- If the emergency significantly alters the product direction, the Group of Deciders documents the impact and any concerns.

### Step 3: Tech Lead Revises

1. The Tech Lead assesses the impact on the current execution plan and design.
2. Revises the design and execution plan to accommodate the emergency.
3. Communicates revised assignments to affected Implementers.
4. If the revision requires stopping or restarting in-progress work, coordinate with affected agents.

### Step 4: Implementation

1. Implementers work on the emergency change following the standard implementation workflow (`implementation.md`), except:
   - The emergency takes priority over all other work.
   - Pre-implementation plan review is still required but should be expedited.
2. The Reviewer reviews the work for quality and correctness. The Reviewer cannot reject emergency changes on grounds of misalignment with the previous execution plan.

### Step 5: Update Artifacts

1. The execution plan is updated to reflect the change.
2. The product design document is updated if the emergency altered the product direction.
3. The emergency and its rationale are added to the Project Rationale.

## Logging

The entire emergency change process must be logged without omission per `logging.md`, including: the original directive, Group of Deciders discussion, plan revisions, and implementation.
