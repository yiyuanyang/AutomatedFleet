# Protocol — Escalation

## Purpose

Defines when and how disputes and decisions are escalated through the authority chain.

## Escalation Levels

### Level 1: Direct Negotiation

Between the Reviewer and the Implementer or Tech Lead.

- **When**: Any disagreement about implementation, code quality, or spec interpretation.
- **How**: Back and forth in the review thread or communication channel. Make substantive arguments — cite the rule, the spec, the technical merit.
- **Requirement**: At least one round of documented negotiation must occur before escalating.

### Level 2: Group of Deciders

- **When**: Direct negotiation fails on a question of product rule or product design interpretation. Or the Tech Lead argues the execution plan should change.
- **How**: The escalating party documents:
  1. The specific question or disagreement.
  2. Both positions with their reasoning.
  3. Why direct negotiation failed.
- **Process**: The Group of Deciders reads the full conversation history and context, then makes a binding call. They do not open further debate. Their decision is final unless escalated to Level 3.

### Level 3: Product Owner

- **When**: The Group of Deciders find the rule genuinely ambiguous on a product-direction question. This should be rare.
- **How**: The Group of Deciders documents:
  1. The specific ambiguity.
  2. Competing interpretations.
  3. Why it matters for the product.
- **Process**: All parties provide initial opinions. The Product Owner decides. Once the decision is made, all parties accept it fully.

## Steering Requests

Separate from dispute escalation, the Auditor and Group of Deciders may request steering from the Product Owner:

- **When**: A decision affects product design or direction and the existing rules don't clearly cover it.
- **Not for**: Technical choices that don't affect product experience. These should be resolved at the Tech Lead / Reviewer level.
- **How**: Submit a steering request with an importance label (low / medium / high / critical) for the Product Owner to prioritize.
- **Process**: The Product Owner responds at their discretion based on the importance label.

## Anti-Patterns

- Do not escalate pure technical preference disputes (algorithm choice, naming conventions) beyond the Reviewer level unless they violate a rule or interface contract.
- Do not skip levels. Direct negotiation must come first.
- Do not re-escalate the same question without new information or changed circumstances.

## Logging

All escalations and steering requests must be logged per `logging.md`, including the question, positions, and outcome.
