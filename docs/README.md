# 📚 EnClose documentation hub

This folder documents the current EnClose static landing page, its source files, browser interactions, development process, and the work needed before production use.

> **Implementation boundary:** this repository contains browser-side HTML, CSS, and JavaScript only. No AI model, CRM, appointment service, contact endpoint, database, or backend API is included.

## 🧭 Reading paths

**New reader:** [Overview](project-overview.md) → [Features](features.md) → [Usage](usage.md) → [Limitations](limitations.md).

**Frontend developer:** [Installation](installation.md) → [Project structure](project-structure.md) → [Architecture](architecture.md) → [Configuration](configuration.md) → [Development](development.md) → [Testing](testing.md).

**Release reviewer:** [Security](security.md) → [Accessibility](accessibility.md) → [Deployment](deployment.md) → [Performance](performance.md) → [Runbooks](runbooks/README.md).

## 📖 Documentation catalogue

| Topic | Guide | Purpose |
|---|---|---|
| Product | [Project overview](project-overview.md) | Goals, audience, scope, non-goals |
| Architecture | [Architecture](architecture.md) | Browser runtime and source relationships |
| Architecture | [System design](system-design.md) | Current and proposed architecture |
| Repository | [Project structure](project-structure.md) | File responsibilities |
| Runtime | [Workflow](workflow.md) | Page loading, navigation, tabs, contact flow |
| Features | [Features](features.md) | Existing page capabilities |
| Setup | [Installation](installation.md) | npm and local preview |
| Setup | [Configuration](configuration.md) | Tailwind and resource paths |
| Usage | [Usage](usage.md) | Visitor and developer guide |
| Interface | [API reference](api.md) | DOM function and form boundary |
| Privacy | [Data and privacy](database.md) | No persistence today, future requirements |
| Privacy | [Data flow](data-flow.md) | Assets, DOM, possible form data |
| Code | [Modules](modules.md) | Logical source responsibilities |
| UI | [Components](components.md) | Page sections and component inventory |
| Quality | [Testing](testing.md) | Verification checklist |
| Operations | [Deployment](deployment.md) | Static hosting practices |
| Security | [Security](security.md) | Risks and controls |
| Inclusion | [Accessibility](accessibility.md) | Semantics, keyboard, focus, forms |
| Quality | [Performance](performance.md) | CSS, images, fonts, remote resources |
| Quality | [Limitations](limitations.md) | Existing defects and missing capabilities |
| Planning | [Future scope](future-scope.md) | Prioritized next steps |
| Reference | [Glossary](glossary.md) | Project terminology |
| Reference | [References](references.md) | Official technology documentation |
| Reference | [FAQ](faq.md) | Common questions |
| Support | [Troubleshooting](troubleshooting.md) | Preview and interaction problems |
| Engineering | [Development](development.md) | Code quality and PR process |
| Visual | [Diagrams](diagrams/README.md) | Editable Mermaid diagrams |
| Decisions | [ADRs](adr/README.md) | Design decision history |
| Operations | [Runbooks](runbooks/README.md) | Local development and release procedures |

## ✅ Current implementation facts

- Main page markup: `docs/index.html`.
- Compiled stylesheet: `docs/style.css`.
- Tailwind input: `src/input.css`.
- Tab helper: `main.js`.
- Site logo: `docs/img/logo.png`.
- Contact form action: `/action_page.php`, not implemented in this repository.
- No API server or persistent data store is included.

## 📌 Documentation maintenance rule

When markup, styling, JavaScript, assets, or build commands change, update the corresponding guides and Mermaid diagrams. Keep implemented behaviour separate from plans and recommendations.
