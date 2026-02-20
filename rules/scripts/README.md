# Scripts Directory

This directory contains automation scripts that support Fleet operations. Scripts reduce manual burden on agents and ensure consistent process execution.

## Planned Scripts

| Script | Purpose | Status |
| ------ | ------- | ------ |
| Log capture | Automatically capture agent output and append to the project log | Planned |
| PR review logger | Extract review threads from GitHub PRs and format as log entries | Planned |
| Status transition | Update execution plan status when tasks move between stages | Planned |
| Precedent flagger | Scan debate logs and flag entries that meet precedent criteria | Planned |
| Agent spin-up | Bootstrap an agent instance with the correct role document and context | Planned |
| Audit report generator | Compile audit findings into a structured report | Planned |

## Conventions

- Scripts should be idempotent where possible.
- Scripts must log their own execution per `rules/protocols/logging.md`.
- Scripts are subordinate rules — they must not contradict the Constitution.
