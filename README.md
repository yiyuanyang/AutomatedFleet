# AutomatedFleet

A distributed multi-agent code generation framework. Unlike traditional single-agent approaches, AutomatedFleet orchestrates a swarm of specialized agents collaborating on complex software projects.

## Vision

Transform software development from individual agent tasks to **coordinated fleet operations**:
- **Distribute complexity** across multiple coding agents working in parallel
- **Specialize by function** — different agents for different architectural layers
- **Real-time collaboration** via modern code review workflows (not markdown files)
- **Protocol-driven consistency** enforced by automation, not manual oversight

## Core Principles

### 1. Fleet, Not Individual
- Multiple coding agents (Claude Code instances) working simultaneously
- Task distribution and workload balancing
- Conflict resolution and merge coordination

### 2. Specialization by Role
| Role | Responsibility |
|------|---------------|
| **Tech Lead** | Defines interfaces, protocols, architectural decisions |
| **Code Reviewer** (Codex-like) | Reviews diffs, enforces standards, approves changes |
| **Coding Agents** (Fleet) | Implement features, fix bugs, write tests |
| **Protocol Officer** | Monitors adherence, escalates violations, maintains tooling |

### 3. Modern Code Review Workflow
- **No markdown files** for comments/feedback
- GitHub-style **diff comments** on actual code changes
- **Approval gates** with required reviewers
- **CI/CD integration** for automated checks

### 4. Script-Driven Consistency
- Process enforced by **executable scripts**, not documentation
- **Protocol as code** — validation, linting, enforcement automated
- **Self-healing** — detects drift, auto-corrects or escalates

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                     AUTOMATEDFLEET                          │
├─────────────────────────────────────────────────────────────┤
│  Task Router        │  Distributes work to available agents  │
├─────────────────────────────────────────────────────────────┤
│  Agent Fleet        │  Multiple Claude Code instances        │
│  (Coding Agents)    │  Working on different tasks/modules    │
├─────────────────────────────────────────────────────────────┤
│  Tech Lead Agent    │  Interface definitions, protocol docs  │
├─────────────────────────────────────────────────────────────┤
│  Review Interface   │  GitHub PRs / Custom diff review tool  │
├─────────────────────────────────────────────────────────────┤
│  Protocol Officer   │  Validation scripts, drift detection   │
└─────────────────────────────────────────────────────────────┘
```

## Workflow

1. **Feature Request** → Task Router analyzes and decomposes
2. **Interface Definition** → Tech Lead defines contracts/APIs
3. **Parallel Implementation** → Fleet agents code different modules
4. **Continuous Review** → Code Reviewer examines diffs, comments inline
5. **Integration** → Protocol Officer validates adherence, runs checks
6. **Deployment** → Automated pipeline ships the code

## Key Differences from TheResearcher

| Aspect | TheResearcher | AutomatedFleet |
|--------|--------------|----------------|
| Agents | Sequential (Claude → Codex) | Parallel (Fleet of Claudes) |
| Review | Markdown file exchange | Real diff comments (GitHub-like) |
| Protocol | Document-based enforcement | Script-based, executable |
| Scale | Single-threaded | Distributed, concurrent |
| Feedback | Round-based cycles | Continuous, event-driven |

## Brainstorming & Development

This project itself will be developed via:
1. **Feature brainstorming sessions** — Ideation with Opus/Kimi
2. **Protocol definition** — Tech Lead role establishes contracts
3. **Fleet implementation** — Distributed agent coding
4. **Continuous debugging** — Protocol Officer monitors and fixes
5. **Evolution** — Self-improving framework

## Getting Started

TBD — This is the seed. The first task is defining the core protocol and tooling.

## Questions to Resolve

- How do agents coordinate without conflicts? (Merge strategies, locking)
- What's the minimum viable review interface? (GitHub API vs custom)
- How to distribute tasks optimally? (Dependency graphs, agent availability)
- What's the protocol for interface changes? (Versioning, migration)
- How to debug distributed agent failures? (Observability, tracing)

---

*Status: Seed README — Direction set, implementation TBD*
