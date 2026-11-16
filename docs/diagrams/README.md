# 🗺️ Diagram Catalogue

This directory stores editable Mermaid source diagrams. GitHub renders Mermaid in supported Markdown contexts, so the source remains reviewable and maintainable without fabricated screenshots or unverified exports.

## Current architecture and workflows

| Source | Diagram type | Purpose |
|---|---|---|
| [system-context.mmd](system-context.mmd) | Context flow | Website boundary and visitor |
| [asset-delivery.mmd](asset-delivery.mmd) | Sequence | Static asset request lifecycle |
| [page-navigation.mmd](page-navigation.mmd) | Flowchart | Page sections and navigation |
| [tab-state.mmd](tab-state.mmd) | State diagram | Intended service-panel state |
| [development-workflow.mmd](development-workflow.mmd) | Flowchart | Local edit, Tailwind and preview |
| [deployment.mmd](deployment.mmd) | Flowchart | Static release and rollback |
| [error-handling.mmd](error-handling.mmd) | Flowchart | Broken asset, panel and form boundaries |

## Data-flow views

| Source | Level | Purpose |
|---|---|---|
| [dfd-level-0.mmd](dfd-level-0.mmd) | DFD Level 0 | Visitor and static website context |
| [dfd-level-1.mmd](dfd-level-1.mmd) | DFD Level 1 | Asset delivery, rendering, interaction and form boundary |
| [form-boundary.mmd](form-boundary.mmd) | Feature flow | Current missing form handler and future service branch |

A Level 2 data-flow diagram is not useful for the current project because no backend processing or persistence pipeline exists.

## User and future integration views

| Source | Purpose | Status |
|---|---|---|
| [use-case.mmd](use-case.mmd) | Visitor and maintainer use cases | Current scope plus explicit limitation |
| [future-service-integration.mmd](future-service-integration.mmd) | Proposed secure service boundary | Proposed, not implemented |

## UML and database diagrams intentionally omitted

A class diagram, database ERD, schema diagram, API interaction diagram, and infrastructure deployment topology would imply classes, persistence, service endpoints, or infrastructure that are not present in this repository. Add them only when real implementation details exist.

## Maintenance rules

1. Keep source diagrams in this directory.
2. Embed a fenced `mermaid` version in a guide when that improves readability.
3. Label future architecture as proposed.
4. Update the diagram in the same change as the implementation.
5. Do not create a rendered image and call it a real screenshot of the app.
