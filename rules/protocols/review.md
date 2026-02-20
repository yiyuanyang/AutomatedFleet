# Protocol — Review

## Purpose

Defines how the Reviewer evaluates work at two stages: pre-implementation (plan review) and post-implementation (code review).

## Pre-Implementation Review

When an Implementer proposes a fragment implementation plan:

1. **Check alignment**: Does the proposed plan match the execution plan fragment? Are there deviations?
2. **Check interfaces**: Does the plan correctly reference and implement the specified interface contracts?
3. **Check test plan**: Are the proposed test cases sufficient? Do they cover edge cases?
4. **Provide feedback**: If changes are needed, be specific and actionable. Cite the execution plan, interface contract, or quality standard.
5. **Confirm or request changes**: Back and forth until the plan is solid.

Only confirm when the implementation plan is ready for execution. Do not confirm prematurely.

## Post-Implementation Review

When an Implementer submits completed work via pull request:

### Checklist

1. **Spec compliance**: Does the implementation match the execution plan fragment as written?
2. **Interface compliance**: Are all interface contracts honored?
3. **Tests exist**: Did the Implementer write tests for all implemented functionality?
4. **Tests are correct**: Do the tests actually verify the right behavior? Are there missing edge cases?
5. **Tests pass**: Do all tests pass?
6. **Code quality**: Is the code clean, readable, and maintainable? Does it follow project conventions?
7. **No scope creep**: Did the Implementer implement what was specified, and only what was specified?

### Providing Feedback

- Be specific. Reference the exact line, file, or requirement.
- Be actionable. State what needs to change, not just that something is wrong.
- Distinguish between blocking issues (must fix) and suggestions (could improve).
- All feedback is recorded in the pull request for logging purposes.

### Approval

- Approve only when all checklist items are satisfied.
- If the Implementer disputes a finding, negotiate directly. If negotiation fails, escalate per `escalation.md`.

## Handling Execution Plan Changes

If the Tech Lead argues that the execution plan needs to change (to better reflect the spirit of the product design):

1. The Reviewer does not make this call alone.
2. Escalate to the Group of Deciders with the Tech Lead's reasoning and the current plan.
3. The Group of Deciders decides.

## Emergency Changes

When the Product Owner injects an emergency change:

- The Reviewer cannot reject it on grounds of misalignment with the existing execution plan.
- Review the revised implementation for quality and correctness, not for plan alignment.
- See `emergency-change.md` for the full procedure.

## Logging

All review feedback, approvals, rejections, and disputes must be logged per `logging.md`.
