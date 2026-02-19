# AutomatedFleet

Distributed multi-agent code generation framework. A swarm of specialized agents collaborating on complex software projects.

## Architecture Decisions

| Aspect | Decision |
|---|---|
| **Agent Runtime** | OpenClaw as assistant overseeing subagents and crons |
| **Repo Structure** | Monorepo |
| **Human-in-the-loop** | Escalate only when blocked; agents work on other sub-items while waiting for steer |
| **First Target** | Infrastructure setup itself |
| **Cost Control** | Configurable model tiers (Kimi for routine, Opus for critical) |

## Core Roles

| Role | Function |
|---|---|
| **Tech Lead** | Defines interfaces, protocols, architectural decisions |
| **Code Reviewer** | Reviews diffs, enforces standards (GitHub-style) |
| **Fleet Agents** | Multiple coding agents on distributed tasks |
| **Orchestrator** | OpenClaw assistant managing the fleet |

## Coordination Model

1. **Git-based**: Agents work in branches, propose PRs
2. **Module Ownership**: Strict file boundaries prevent conflicts
3. **Interface Contracts**: Tech Lead defines `src/contracts/`, agents code against them
4. **Merge Queue**: Sequential PR merges with auto-rebase

## Pending Items / User Steer

Agents can flag items needing human input while continuing work on other sub-tasks. No blocking on single decisions.

## Cost Strategy

- **Routine work**: Kimi K2.5 (near-zero cost)
- **Critical design**: Opus (high reasoning)
- **Standard coding**: Sonnet 4.6 (balanced)

## Status

Infrastructure setup in progress. See `README.md` for architecture brainstorm.

---

*Last updated: 2026-02-19*