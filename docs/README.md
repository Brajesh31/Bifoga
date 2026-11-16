# 📚 EnClose documentation hub

Welcome to the technical documentation for **EnClose**, the static AI consultation and education landing-page concept in the Bifoga repository.

> [!IMPORTANT]
> This repository currently provides a static browser experience. It does not include an AI inference service, booking engine, CRM, application API, database, authentication, or contact-form handler. Future designs in these documents are labelled as proposals, not shipped capabilities.

## 🧭 Choose a reading path

- **Understand the project:** [Overview](project-overview.md) → [Features](features.md) → [Limitations](limitations.md) → [Future scope](future-scope.md).
- **Start developing:** [Installation](installation.md) → [Configuration](configuration.md) → [Project structure](project-structure.md) → [Development](development.md) → [Testing](testing.md).
- **Understand engineering:** [Architecture](architecture.md) → [System design](system-design.md) → [Data flow](data-flow.md) → [Modules](modules.md) → [Components](components.md) → [Diagrams](diagrams/README.md).
- **Prepare a release:** [Security](security.md) → [Accessibility](accessibility.md) → [Performance](performance.md) → [Deployment](deployment.md) → [Release process](release-process.md) → [Runbooks](runbooks/README.md).

## 📖 Complete documentation catalogue

| Area | Document | Coverage |
|---|---|---|
| Product | [Project overview](project-overview.md) | Purpose, audience, goals and non-goals |
| Product | [Features](features.md) | Current page capabilities and boundaries |
| Product | [Usage](usage.md) | Visitor and maintainer usage |
| Product | [Limitations](limitations.md) | Missing and incomplete capabilities |
| Planning | [Future scope](future-scope.md) | Prioritized potential improvements |
| Architecture | [Architecture](architecture.md) | Static runtime and source relationships |
| Architecture | [System design](system-design.md) | Current architecture and evolution |
| Architecture | [Data flow](data-flow.md) | Browser, assets and form boundary |
| Architecture | [Modules](modules.md) | Source-file responsibilities |
| Architecture | [Components](components.md) | Page regions and interaction patterns |
| Architecture | [Diagrams](diagrams/README.md) | Editable Mermaid sources |
| Repository | [Project structure](project-structure.md) | Directory and file responsibilities |
| Setup | [Installation](installation.md) | Node.js, npm and local preview |
| Setup | [Configuration](configuration.md) | Tailwind and environment boundaries |
| Development | [Development](development.md) | Editing and contribution workflow |
| Development | [Testing](testing.md) | Manual checks and CI baseline |
| Development | [API reference](api-reference.md) | Browser helper and absence of HTTP API |
| Development | [Legacy interface notes](api.md) | Short interface summary |
| Data | [Database and persistence](database.md) | No current database; future safeguards |
| Operations | [Deployment](deployment.md) | Static hosting guidance |
| Operations | [Release process](release-process.md) | Release preparation and rollback |
| Operations | [Runbooks](runbooks/README.md) | Local preview, release and incident response |
| Security | [Security](security.md) | Threat boundaries and controls |
| Accessibility | [Accessibility](accessibility.md) | Semantic markup and keyboard behavior |
| Performance | [Performance](performance.md) | Asset, CSS and runtime considerations |
| Support | [Troubleshooting](troubleshooting.md) | Common development issues |
| Support | [FAQ](faq.md) | Frequently asked questions |
| Reference | [Glossary](glossary.md) | Project terminology |
| Reference | [References](references.md) | Official technical resources |
| Governance | [Architecture decisions](adr/README.md) | Decision records |
 
## 🔎 Verified implementation inventory

| Path | Role |
|---|---|
| `docs/index.html` | Main static page |
| `docs/style.css` | Served stylesheet output |
| `src/input.css` | Tailwind/CSS source entry point |
| `main.js` | Browser-side menu helper |
| `docs/img/logo.png` | Existing project logo |
| `tailwind.config.js` | Tailwind content configuration |
| `package.json` / `package-lock.json` | npm scripts and dependency lock |
| `.github/workflows/` | Existing README automation plus repository checks |

## 🧱 Diagram conventions

Mermaid files in [diagrams/](diagrams/README.md) are editable source. The current-state diagrams describe the static website. Any diagram that includes a future API, database, AI service, or form processor is explicitly marked as proposed.

## 🛠️ Keeping documentation accurate

When changing HTML, CSS, JavaScript, package scripts, assets, or hosting configuration:
1. Update the relevant guide and source inventory.
2. Update affected diagrams.
3. Verify all file paths and commands against the repository.
4. Run the available CI checks.
5. Separate shipped behavior from proposals and known gaps.

Do not add empty directories, fake screenshots, invented metrics, or API/database documentation that implies nonexistent systems.
