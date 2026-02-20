# Protocol — Architecture and Planning

## Purpose

Defines how the Tech Lead translates a finalized product design into an executable plan: architecture, interfaces, task breakdown, and parallelization strategy.

## Preconditions

- The product design is finalized (see `product-design.md`).
- The Project Rationale is available.
- The Tech Lead and the technical member of the Group of Deciders are active.

## Process

### Step 1: Propose the Implementation Plan

The Tech Lead produces a comprehensive implementation plan covering:

1. **System architecture**: Technology choices, overall structure, deployment model.
2. **Module boundaries and interface contracts**: Clear separation of concerns, defined inputs/outputs between modules.
3. **Task breakdown**: The project decomposed into implementable fragments. Each fragment should be assignable to a single Implementer.
4. **Dependency graph**: Which fragments depend on which. Identify what can run in parallel and what must be sequential.
5. **Parallelization strategy**: How many Implementers to spin up, which fragments to parallelize, coordination mechanisms.
6. **Inter-agent coordination**: Branching strategy, communication protocols, integration points.

### Step 2: Review with Technical Group of Deciders Member

1. The technical member of the Group of Deciders reviews the plan. This member carries the full history of product deliberations and can assess whether the architecture serves the product intent.
2. Back and forth until both parties are satisfied.
3. Focus areas: Does the architecture support the product goals? Are there technical risks? Is the breakdown reasonable?

### Step 3: Escalation (if needed)

If the Tech Lead and technical reviewer cannot align, or if the implementation reveals that the product design needs revision:

1. Document the specific issue: what is infeasible, what constraints conflict, what alternatives exist.
2. Escalate to the full Group of Deciders.
3. The Group of Deciders reads the context and makes a binding decision.
4. If the Group of Deciders cannot resolve it, escalate to the Product Owner per `escalation.md`.

### Step 4: Finalize the Execution Plan

1. Once aligned, the execution plan is finalized.
2. The execution plan becomes the source of truth for the project realm. The Reviewer and Implementers follow it as written.

**Output**:
- Finalized execution plan document.
- Interface contracts for each module boundary.
- Task assignments with fragment specs.

## After This Protocol

The Tech Lead begins spinning up Implementer agents per `implementation.md`.

## Logging

All planning discussions, design decisions, and trade-offs must be logged per `logging.md`.
