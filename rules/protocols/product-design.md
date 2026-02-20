# Protocol — Product Design

## Purpose

Defines how the product design is created through deliberation between the Product Owner, Group of Deciders, and the Auditor. The output is a finalized product design document and its accompanying Project Rationale.

## Preconditions

- The Product Owner has a product idea.
- The Auditor is active.

## Process

### Step 1: Assemble the Group of Deciders

The Product Owner selects the Group of Deciders for this product:

1. Define the product idea at a high level.
2. Choose member backgrounds that match the product's domain (at minimum: one technical, one business-model-oriented, one product-user-oriented).
3. Add additional members to represent specific user segments if the product serves multiple audiences.
4. Assign voting shares to each member.
5. Provide each member's prompt with their identity, background, and interest lean.

**Output**: Group of Deciders assembled and ready for deliberation.

### Step 2: Product Deliberation

The Auditor facilitates deliberation between the Product Owner and the Group of Deciders:

1. The Product Owner presents the product vision.
2. Each Group of Deciders member responds from their background and perspective.
3. The Auditor relays opinions and context between parties, ensuring all perspectives are heard.
4. Members raise concerns, propose alternatives, argue trade-offs.
5. Multiple rounds of back-and-forth until the product direction converges.

**During deliberation, document everything**:
- Arguments for and against each decision.
- Abandoned ideas and why they were abandoned.
- Trade-offs considered.
- Dissenting opinions.

This record becomes the **Project Rationale**.

### Step 3: Finalize the Product Design

1. The Group of Deciders votes on the final product design.
2. The Product Owner reviews and approves (or requests changes).
3. Once approved, the product design document is finalized and carries the force of rule (Constitution Article III).

**Output**:
- Finalized product design document (stored at a project-specific path).
- Project Rationale document (stored alongside the product design).

## After This Protocol

The product design is handed to the Tech Lead, who begins the architecture and planning process (see `architecture-planning.md`).

## Logging

All deliberation sessions must be logged without omission per `logging.md`. The Project Rationale is a permanent artifact that may be referenced in future decisions.
