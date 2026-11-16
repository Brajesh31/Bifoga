# 🗂️ Project Structure

This tree reflects the repository's static-site architecture and the documentation/automation additions. It intentionally does not invent backend, database, test-framework, or application-component directories that are not present.

## Repository tree

```text
Bifoga/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.yml
│   │   ├── config.yml
│   │   ├── documentation.yml
│   │   └── feature_request.yml
│   ├── workflows/
│   │   ├── ci.yml
│   │   ├── security.yml
│   │   └── update-readme.yml
│   └── PULL_REQUEST_TEMPLATE.md
├── assets/
│   ├── README.md
│   └── banners/
│       └── enclose-banner.svg
├── docs/
│   ├── adr/
│   │   ├── README.md
│   │   ├── 0001-static-first.md
│   │   ├── 0002-contact-form-boundary.md
│   │   └── 0003-accessible-interactions.md
│   ├── diagrams/
│   │   ├── README.md
│   │   ├── system-context.mmd
│   │   ├── page-navigation.mmd
│   │   ├── form-boundary.mmd
│   │   ├── asset-delivery.mmd
│   │   ├── development-workflow.mmd
│   │   └── future-service-integration.mmd
│   ├── runbooks/
│   │   ├── README.md
│   │   ├── local-preview.md
│   │   ├── static-release.md
│   │   └── incident-response.md
│   ├── img/logo.png
│   ├── index.html
│   ├── style.css
│   └── *.md (project, engineering, quality and operational guides)
├── src/
│   └── input.css
├── .editorconfig
├── .env.example
├── .gitattributes
├── .gitignore
├── CHANGELOG.md
├── CITATION.cff
├── CODEOWNERS
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── GOVERNANCE.md
├── LICENSE
├── MAINTAINERS.md
├── README.md
├── ROADMAP.md
├── SECURITY.md
├── SUPPORT.md
├── main.js
├── package.json
├── package-lock.json
└── tailwind.config.js
```

## 1. Application and asset files

| Path | Responsibility | Change guidance |
|---|---|---|
| `docs/index.html` | Main page markup and copy | Preserve semantic structure and update navigation IDs together |
| `docs/style.css` | CSS served by the page | Regenerate after Tailwind source changes |
| `docs/img/logo.png` | Existing brand image | Preserve original asset |
| `src/input.css` | Tailwind entry and authored CSS | Main styling source |
| `main.js` | Browser-side menu helper | Keep DOM assumptions and control/panel IDs consistent |
| `tailwind.config.js` | Tailwind content and theme settings | Update scan paths when HTML files change |
| `package.json` | npm scripts and development dependencies | Review every dependency/script change |
| `package-lock.json` | Locked npm dependency graph | Update with npm, commit with package metadata |

## 2. Documentation structure

- Root Markdown files describe repository entry points, contribution, governance, security, support, roadmap, and release history.
- `docs/README.md` is the documentation index.
- Top-level `docs/*.md` files cover project, architecture, development, quality, and operations.
- `docs/diagrams/` stores editable Mermaid source.
- `docs/adr/` stores architecture decisions.
- `docs/runbooks/` stores repeatable operational procedures.

## 3. GitHub automation

| Path | Responsibility |
|---|---|
| `.github/ISSUE_TEMPLATE/` | Structured bug, feature, and documentation requests |
| `.github/PULL_REQUEST_TEMPLATE.md` | Review and verification checklist |
| `.github/workflows/ci.yml` | Basic static source and documentation checks |
| `.github/workflows/security.yml` | Scheduled and change-triggered npm audit |
| `.github/workflows/update-readme.yml` | Existing README update automation, preserved |

## 4. Build and deployment boundary

The configured Tailwind script watches `src/input.css` and writes `docs/style.css`. A static host can serve `docs/`. The actual hosting provider is not declared in this repository.

## 5. Directories intentionally not added

No empty `backend/`, `database/`, `models/`, `components/`, `services/`, or `tests/` directory is added because the corresponding implementation does not exist. Add those directories only with real code and a documented purpose.
