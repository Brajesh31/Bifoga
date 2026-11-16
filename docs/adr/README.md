# 🧠 Architecture Decision Records

Architecture Decision Records capture decisions that affect project structure, runtime boundaries, dependencies, security, or long-term maintenance.

## Status vocabulary

- **Proposed**: under discussion.
- **Accepted**: approved for implementation or retained as the current decision.
- **Superseded**: replaced by a later ADR.
- **Deprecated**: no longer recommended.

## Current records

| ADR | Decision | Status |
|---|---|---|
| [0001: Static-first architecture](0001-static-first.md) | Keep the current site static unless a validated requirement needs a service | Accepted |
| [0002: Contact form boundary](0002-contact-form-boundary.md) | Do not claim form delivery without a real handler | Accepted |
| [0003: Accessible interactions](0003-accessible-interactions.md) | Use semantic, keyboard-operable controls for interactive UI | Accepted |

Add a new numbered record for significant decisions. Do not rewrite history silently; supersede an earlier record when the decision changes.
