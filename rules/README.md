# Rules Directory — Automated Fleet

All subordinate rules that extend and implement the [Constitution](../CONSTITUTION.md). The Constitution is always the first document read; everything here is subordinate to it.

---

## How This Works

1. Each rule is an individual document covering a specific topic.
2. Each role has a role document in `roles/` that specifies which rules and additional context that role must read.
3. When an agent instance is spun up, the orchestration system loads the Constitution, the role document, and all documents referenced by the role document as always-available context.
4. Roles follow the rules designated to them by their role document.

---

## Role Documents

Role documents define each role's responsibilities and required reading list.

| Role | Document |
| ---- | -------- |
| Group of Deciders | [`roles/group-of-deciders.md`](roles/group-of-deciders.md) |
| The Auditor | [`roles/auditor.md`](roles/auditor.md) |
| Tech Lead | [`roles/tech-lead.md`](roles/tech-lead.md) |
| Implementer | [`roles/implementer.md`](roles/implementer.md) |

The Reviewer is a subsection of the Group of Deciders role document, as the Reviewer is typically the technical member of that group operating in the project realm.

---

## Protocol Documents

Protocols define how specific processes work.

| Protocol | Document | Applicable Roles |
| -------- | -------- | ---------------- |
| Product Design | [`protocols/product-design.md`](protocols/product-design.md) | Product Owner, Group of Deciders, Auditor |
| Architecture & Planning | [`protocols/architecture-planning.md`](protocols/architecture-planning.md) | Tech Lead, Group of Deciders (technical member) |
| Implementation | [`protocols/implementation.md`](protocols/implementation.md) | Tech Lead, Implementer, Reviewer |
| Review | [`protocols/review.md`](protocols/review.md) | Reviewer, Implementer |
| Emergency Changes | [`protocols/emergency-change.md`](protocols/emergency-change.md) | All roles |
| Escalation | [`protocols/escalation.md`](protocols/escalation.md) | All roles |
| Audit | [`protocols/audit.md`](protocols/audit.md) | Auditor |
| Logging | [`protocols/logging.md`](protocols/logging.md) | All roles |

---

## Scripts

Automation scripts that support Fleet operations. See [`scripts/README.md`](scripts/README.md) for the full list and status.

---

## Adding New Rules

1. Create a new document in the appropriate subdirectory (`protocols/`, `scripts/`, or a new category).
2. Add it to this README index.
3. Update the relevant role documents to include it in their required reading list.
4. The Group of Deciders may create product-realm rules; the Auditor may create process-realm rules. Constitutional principles require Product Owner approval to change (Constitution Article VI).
