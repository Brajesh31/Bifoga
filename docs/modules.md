# 🧩 Modules and Responsibilities

## 1. Current module inventory

This repository is intentionally small. It does not use a frontend framework, module bundler, component framework, or backend service. The main responsibilities are separated by file rather than by a large application-module hierarchy.

| Module or file | Responsibility | Important boundary |
|---|---|---|
| `docs/index.html` | Main page markup and content | Static document, not a server template |
| `main.js` | Small browser interaction helper | No API client or persistence layer |
| `src/input.css` | Authored CSS and Tailwind entry point | Source stylesheet |
| `docs/style.css` | Stylesheet served with the page | Generated/compiled output should be regenerated through the configured tool |
| `tailwind.config.js` | Tailwind content scanning and theme configuration | Build-time configuration |
| `package.json` | Project metadata and npm scripts | Development tooling |
| `package-lock.json` | Locked npm dependency graph | Keep synchronized with package metadata |
| `docs/img/logo.png` | Existing logo image | Preserve the original asset |

## 2. Page regions

The HTML page groups content into navigation and page sections. Treat these as content regions, not independently deployable modules. When adding a section:
- Give it a stable, unique ID.
- Add a descriptive navigation link only if the section is intended to be navigable.
- Use semantic landmarks and headings.
- Keep the reading order meaningful without CSS.
- Ensure any interactive controls have an accessible name and keyboard behavior.

## 3. JavaScript responsibility

The existing `openMenu` helper handles a narrow display-toggle responsibility. It is not a general state-management system. It does not:
- Fetch data.
- Call an AI model.
- Submit a contact request through a defined API.
- Store user preferences.
- Authenticate users.
- Manage routes or browser history.

If new browser behavior is introduced, keep each function focused, validate DOM assumptions, avoid unsafe HTML injection, and document its inputs and side effects.

## 4. Styling responsibility

The project uses Tailwind CSS tooling alongside authored CSS. Keep the source stylesheet and generated output in sync. Prefer reusable utility patterns and a consistent design vocabulary. Avoid introducing a second CSS framework without a clear need.

## 5. Recommended future separation

If the site grows, a maintainable next step could be to split repeated page regions into reusable partials or components and introduce a build step only when the complexity justifies it. Do not add empty `components/`, `services/`, or `models/` directories to imply that those modules already exist.

## 6. Change-impact map

| Change | Review these files |
|---|---|
| Page section or copy | `docs/index.html`, README feature descriptions |
| Navigation target | `docs/index.html`, page-flow diagram |
| Tab behavior | `main.js`, related HTML controls/panels, interaction documentation |
| Global style | `src/input.css`, `docs/style.css` generation, responsive checks |
| Tailwind scanning | `tailwind.config.js`, npm scripts |
| Dependency change | `package.json`, `package-lock.json`, installation guide |
| Contact integration | Form markup, new server/service code, privacy and security documentation |
