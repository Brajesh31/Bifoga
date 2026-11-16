# 🗂️ Project structure

## Repository tree

```text
Bifoga/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.yml
│   │   ├── documentation.yml
│   │   └── feature_request.yml
│   ├── workflows/
│   │   ├── docs-check.yml
│   │   ├── site-check.yml
│   │   └── update-readme.yml
│   └── PULL_REQUEST_TEMPLATE.md
├── docs/
│   ├── diagrams/
│   ├── img/logo.png
│   ├── index.html
│   ├── style.css
│   └── guides
├── src/input.css
├── main.js
├── package.json
├── package-lock.json
├── tailwind.config.js
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
└── SUPPORT.md
```

## Application and asset files

| Path | Responsibility | Editing guidance |
|---|---|---|
| `docs/index.html` | Main page structure | Edit content and semantic markup here |
| `docs/style.css` | Generated CSS output | Regenerate after input changes |
| `docs/img/logo.png` | EnClose brand image | Preserve the original asset |
| `src/input.css` | Tailwind entry and custom CSS | Main styling source |
| `main.js` | Service tab helper | Keep DOM IDs and tab markup consistent |
| `tailwind.config.js` | Tailwind content and theme config | Ensure new HTML paths are scanned |
| `package.json` | Scripts and dev dependencies | Keep commands reproducible |
| `package-lock.json` | Locked dependency graph | Update only for intentional dependency changes |

## Repository support files

| File | Responsibility |
|---|---|
| `.editorconfig` | Shared editor defaults |
| `.env.example` | Documents current/future configuration placeholders |
| `.gitattributes` | Git text and line-ending rules |
| `.gitignore` | Excludes local dependencies and logs |
| `README.md` | Entry point and quick start |
| `CHANGELOG.md` | Human-readable changes |
| `CITATION.cff` | Citation metadata |
| `CONTRIBUTING.md` | Contributor process |
| `GOVERNANCE.md` | Project decisions and responsibility |
| `MAINTAINERS.md` | Maintainer ownership |
| `CODE_OF_CONDUCT.md` | Community standards |
| `SECURITY.md` | Security reporting policy |
| `SUPPORT.md` | Help channels and scope |
| `ROADMAP.md` | Planned improvements |
| `LICENSE` | Existing MIT license |

## Source of truth

`docs/style.css` is generated output. Edit `src/input.css` and regenerate CSS. Do not remove the existing stylesheet or logo image.

## Future organization

A future refactor may introduce a `tests/` directory for browser-level checks. A server directory should only be introduced when backend code is genuinely implemented. The current repository has no backend.
